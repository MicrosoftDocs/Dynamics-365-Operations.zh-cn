---
title: 审核应付帐款中的账单和关键数据
description: 本主题介绍如何审核应付帐款中的账单和关键数据。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5bb89f0adce41b045b1f573c4c0e841f78b2248c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440637"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a><span data-ttu-id="62356-103">审核应付帐款中的账单和关键数据</span><span class="sxs-lookup"><span data-stu-id="62356-103">Audit invoices and key data in accounts payable</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="62356-104">在您从供应商处收到针对采购订单上的货物或服务的发票时，该业务流程可能要求首先接收货物或服务，然后才能对发票进行审核以便付款。</span><span class="sxs-lookup"><span data-stu-id="62356-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="62356-105">在您开始前，请确保选择发票匹配 Configuration Key。</span><span class="sxs-lookup"><span data-stu-id="62356-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="62356-106">在 **应付帐款参数** 页面，确保已选择“启用发票匹配验证”选项，已设置 **过帐发票差异** 字段为 **请求批准**，以及已设置 **行匹配政策** 字段为 **三向匹配**。</span><span class="sxs-lookup"><span data-stu-id="62356-106">In the **Accounts payable parameters** page, ensure that the Enable invoice matching validation option is selected, the **Post invoice with discrepancies** field is set to **Require approval**, and the **Line matching policy** field is set to **Three-way matching**.</span></span>

<span data-ttu-id="62356-107">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="62356-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="62356-108">应付帐款经理或会计经理将执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="62356-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="62356-109">创建采购订单</span><span class="sxs-lookup"><span data-stu-id="62356-109">Create a purchase order</span></span>
1. <span data-ttu-id="62356-110">转到 **所有采购订单**。</span><span class="sxs-lookup"><span data-stu-id="62356-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="62356-111">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="62356-111">Click **New**.</span></span>
3. <span data-ttu-id="62356-112">在 **供应商帐户** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="62356-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="62356-113">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="62356-113">Click **OK**.</span></span>
5. <span data-ttu-id="62356-114">单击 **添加行**。</span><span class="sxs-lookup"><span data-stu-id="62356-114">Click **Add line**.</span></span>
6. <span data-ttu-id="62356-115">在 **项目编号** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="62356-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="62356-116">在“操作窗格”上，单击 **采购**。</span><span class="sxs-lookup"><span data-stu-id="62356-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="62356-117">单击 **确认**。</span><span class="sxs-lookup"><span data-stu-id="62356-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="62356-118">将产品收据过帐</span><span class="sxs-lookup"><span data-stu-id="62356-118">Post a product receipt</span></span>
1. <span data-ttu-id="62356-119">在“操作窗格”上，单击 **接收**。</span><span class="sxs-lookup"><span data-stu-id="62356-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="62356-120">单击 **产品收据**。</span><span class="sxs-lookup"><span data-stu-id="62356-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="62356-121">在 **产品收据** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="62356-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="62356-122">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="62356-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="62356-123">记录供应商发票并与产品收据匹配</span><span class="sxs-lookup"><span data-stu-id="62356-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="62356-124">在操作窗格上，单击 **发票 > 发票**。</span><span class="sxs-lookup"><span data-stu-id="62356-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="62356-125">在 **编号** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="62356-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="62356-126">单击 **默认订购数量**，以打开拖放对话框。</span><span class="sxs-lookup"><span data-stu-id="62356-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="62356-127">在 **默认行数量** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="62356-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="62356-128">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="62356-128">Click **OK**.</span></span>
6. <span data-ttu-id="62356-129">单击 **是**。</span><span class="sxs-lookup"><span data-stu-id="62356-129">Click **Yes**.</span></span>
7. <span data-ttu-id="62356-130">单击 **匹配产品收据**。</span><span class="sxs-lookup"><span data-stu-id="62356-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="62356-131">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="62356-131">Click **OK**.</span></span>
9. <span data-ttu-id="62356-132">在操作窗格上，单击 **审核**。</span><span class="sxs-lookup"><span data-stu-id="62356-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="62356-133">单击 **匹配详细信息**。</span><span class="sxs-lookup"><span data-stu-id="62356-133">Click **Matching details**.</span></span>

