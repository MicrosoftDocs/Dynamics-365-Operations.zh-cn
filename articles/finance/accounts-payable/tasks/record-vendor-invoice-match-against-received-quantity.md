---
title: 记录供应商发票和匹配接收的数量
description: 在您从供应商处收到针对采购订单上的货物或服务的发票时，该业务流程可能要求首先接收货物或服务，然后才能对发票进行审核以便付款。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 66f3b3444b9ff6a93d83c97f1d962c3bdb0699c9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227104"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a><span data-ttu-id="f2bb0-103">记录供应商发票和匹配接收的数量</span><span class="sxs-lookup"><span data-stu-id="f2bb0-103">Record vendor invoice and match against received quantity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2bb0-104">在您从供应商处收到针对采购订单上的货物或服务的发票时，该业务流程可能要求首先接收货物或服务，然后才能对发票进行审核以便付款。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="f2bb0-105">在您开始前，请确保选择发票匹配 Configuration Key。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="f2bb0-106">在应付帐款参数页面，确保已选择“启用发票匹配验证”选项，已设置“过帐发票差异”字段为“请求批准”，以及已设置“行匹配政策”字段为三向匹配。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="f2bb0-107">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="f2bb0-108">应付帐款经理或会计经理将执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="f2bb0-109">创建采购订单</span><span class="sxs-lookup"><span data-stu-id="f2bb0-109">Create a purchase order</span></span>
1. <span data-ttu-id="f2bb0-110">转到“所有采购订单”。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="f2bb0-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-111">Click New.</span></span>
3. <span data-ttu-id="f2bb0-112">在“供应商帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f2bb0-113">在“供应商帐户”字段中，输入一个供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="f2bb0-114">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-114">Click OK.</span></span>
6. <span data-ttu-id="f2bb0-115">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-115">Click Add line.</span></span>
7. <span data-ttu-id="f2bb0-116">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="f2bb0-117">在操作窗格上，单击“采购”。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="f2bb0-118">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="f2bb0-119">将产品收据过帐</span><span class="sxs-lookup"><span data-stu-id="f2bb0-119">Post a product receipt</span></span>
1. <span data-ttu-id="f2bb0-120">在操作窗格上，单击“接收”。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="f2bb0-121">单击“产品收据”。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-121">Click Product receipt.</span></span>
3. <span data-ttu-id="f2bb0-122">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f2bb0-123">在“产品收据”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="f2bb0-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="f2bb0-125">记录供应商发票并与产品收据匹配</span><span class="sxs-lookup"><span data-stu-id="f2bb0-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="f2bb0-126">在操作窗格上，单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="f2bb0-127">单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-127">Click Invoice.</span></span>
3. <span data-ttu-id="f2bb0-128">在“编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="f2bb0-129">单击“默认订购数量”，以打开拖放对话框。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="f2bb0-130">在“默认行数量”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="f2bb0-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-131">Click OK.</span></span>
7. <span data-ttu-id="f2bb0-132">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-132">Click Yes.</span></span>
8. <span data-ttu-id="f2bb0-133">单击“匹配产品收据”。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="f2bb0-134">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-134">Click OK.</span></span>
10. <span data-ttu-id="f2bb0-135">在操作窗格上，单击“审核”。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="f2bb0-136">单击“匹配详细信息”。</span><span class="sxs-lookup"><span data-stu-id="f2bb0-136">Click Matching details.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]