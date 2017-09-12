--- 
title: "审核应付帐款中的发票和关键数据"
description: "在您从供应商处收到针对采购订单上的货物或服务的发票时，该业务流程可能要求首先接收货物或服务，然后才能对发票进行审核以便付款。"
author: saraschi2
manager: AnnBe
ms.date: 02/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 095001a74566e0246951ad9631a8076c72b84f1c
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a><span data-ttu-id="06984-103">审核应付帐款中的发票和关键数据</span><span class="sxs-lookup"><span data-stu-id="06984-103">Audit invoices and key data in accounts payable</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="06984-104">在您从供应商处收到针对采购订单上的货物或服务的发票时，该业务流程可能要求首先接收货物或服务，然后才能对发票进行审核以便付款。</span><span class="sxs-lookup"><span data-stu-id="06984-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="06984-105">在您开始前，请确保选择发票匹配 Configuration Key。</span><span class="sxs-lookup"><span data-stu-id="06984-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="06984-106">在应付帐款参数页面，确保已选择“启用发票匹配验证”选项，已设置“过帐发票差异”字段为“请求批准”，以及已设置“行匹配政策”字段为三向匹配。</span><span class="sxs-lookup"><span data-stu-id="06984-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="06984-107">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="06984-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="06984-108">应付帐款经理或会计经理将执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="06984-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="06984-109">创建采购订单</span><span class="sxs-lookup"><span data-stu-id="06984-109">Create a purchase order</span></span>
1. <span data-ttu-id="06984-110">转到“所有采购订单”。</span><span class="sxs-lookup"><span data-stu-id="06984-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="06984-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="06984-111">Click New.</span></span>
3. <span data-ttu-id="06984-112">在“供应商帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="06984-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="06984-113">在“供应商帐户”字段中，输入一个供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="06984-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="06984-114">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="06984-114">Click OK.</span></span>
6. <span data-ttu-id="06984-115">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="06984-115">Click Add line.</span></span>
7. <span data-ttu-id="06984-116">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="06984-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="06984-117">在操作窗格上，单击“采购”。</span><span class="sxs-lookup"><span data-stu-id="06984-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="06984-118">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="06984-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="06984-119">将产品收据过帐</span><span class="sxs-lookup"><span data-stu-id="06984-119">Post a product receipt</span></span>
1. <span data-ttu-id="06984-120">在操作窗格上，单击“接收”。</span><span class="sxs-lookup"><span data-stu-id="06984-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="06984-121">单击“产品收据”。</span><span class="sxs-lookup"><span data-stu-id="06984-121">Click Product receipt.</span></span>
3. <span data-ttu-id="06984-122">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="06984-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="06984-123">在“产品收据”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="06984-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="06984-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="06984-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="06984-125">记录供应商发票并与产品收据匹配</span><span class="sxs-lookup"><span data-stu-id="06984-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="06984-126">在操作窗格上，单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="06984-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="06984-127">单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="06984-127">Click Invoice.</span></span>
3. <span data-ttu-id="06984-128">在“编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="06984-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="06984-129">单击“默认订购数量”，以打开拖放对话框。</span><span class="sxs-lookup"><span data-stu-id="06984-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="06984-130">在“默认行数量”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="06984-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="06984-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="06984-131">Click OK.</span></span>
7. <span data-ttu-id="06984-132">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="06984-132">Click Yes.</span></span>
8. <span data-ttu-id="06984-133">单击“匹配产品收据”。</span><span class="sxs-lookup"><span data-stu-id="06984-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="06984-134">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="06984-134">Click OK.</span></span>
10. <span data-ttu-id="06984-135">在操作窗格上，单击“审核”。</span><span class="sxs-lookup"><span data-stu-id="06984-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="06984-136">单击“匹配详细信息”。</span><span class="sxs-lookup"><span data-stu-id="06984-136">Click Matching details.</span></span>


