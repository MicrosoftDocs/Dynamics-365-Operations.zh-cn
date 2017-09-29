---
title: "供应商与客户协作"
description: "本主题介绍您在 Finance and Operations 中如何使用供应商协作处理采购订单和监控托运库存。"
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: eaa8f1f71fb15dff8035cb73d198c980e7b364f1
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---

# <a name="vendor-collaboration-with-customers"></a><span data-ttu-id="f5a1b-103">供应商与客户协作</span><span class="sxs-lookup"><span data-stu-id="f5a1b-103">Vendor collaboration with customers</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f5a1b-104">本主题介绍您在 Finance and Operations 中如何使用供应商协作处理采购订单和监控托运库存。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-104">This topic describes how you can use vendor collaboration in Finance and Operations to work with POs and to monitor consignment inventory.</span></span>

<span data-ttu-id="f5a1b-105">本主题介绍您在 Microsoft Finance and Operations 中如何使用供应商协作处理客户。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-105">This topic describes how you can use vendor collaboration to work with customers in Microsoft Finance and Operations.</span></span> <span data-ttu-id="f5a1b-106">包括关于如何监控和响应采购订单，以及如何监控托运库存的信息。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-106">It includes information about how to monitor and respond to purchase orders, and how to monitor consignment inventory.</span></span> <span data-ttu-id="f5a1b-107">还可以使用供应商协作处理发票。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-107">It's also possible to use vendor collaboration to work with invoices.</span></span> <span data-ttu-id="f5a1b-108">有关详细信息，请参阅[供应商协作开票工作区](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace)。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-108">For more information, see [Vendor collaboration invoicing workspace](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace).</span></span>

## <a name="working-with-purchase-orders"></a><span data-ttu-id="f5a1b-109">处理采购订单</span><span class="sxs-lookup"><span data-stu-id="f5a1b-109">Working with purchase orders</span></span>
<span data-ttu-id="f5a1b-110">“**采购订单确认**”工作区允许您响应发送给您审核的采购订单。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-110">The **Purchase order confirmation** workspace enables you to respond to the PO’s that have been sent to you for review.</span></span> <span data-ttu-id="f5a1b-111">您还可以查看正在等待客户操作的采购订单的信息，以及已确认但仍然未结的采购订单的信息。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-111">It also enables you to view information about POs that are awaiting action from the customer, and POs that have been confirmed, but are still open.</span></span> <span data-ttu-id="f5a1b-112">“**采购订单确认**”工作区有三个列表：</span><span class="sxs-lookup"><span data-stu-id="f5a1b-112">There are three lists in the **Purchase order confirmation** workspace:</span></span>

-   <span data-ttu-id="f5a1b-113">**要审核的采购订单** - 此列表显示已经发送给您并且正在等待您响应的采购订单。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-113">**Purchase orders for review** -This list shows POs that have been sent to you and are awaiting a response from you.</span></span> <span data-ttu-id="f5a1b-114">您做出响应后，采购订单将从列表中消失。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-114">After you respond, the PO disappears from the list.</span></span> <span data-ttu-id="f5a1b-115">如果在您响应采购订单之前，客户向您发送了采购订单的新版本，则仅显示最新版本。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-115">If the customer sends you a new version of the PO before you’ve responded to the previous one, only the latest version is shown.</span></span>
-   <span data-ttu-id="f5a1b-116">**正在等待客户操作** - 此列表可以查看您已经响应，但客户尚未确认的采购订单。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-116">**Awaiting customer action** - This list allows you to see POs that you’ve responded to, but have not yet been confirmed by the customer.</span></span> <span data-ttu-id="f5a1b-117">如果您接受了 PO，您可以在此列表中进行监控，直到状态更改为“**已确认**”。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-117">If you accepted the PO, you can monitor it in this list until the status changes to **Confirmed**.</span></span> <span data-ttu-id="f5a1b-118">如果您拒绝 PO 或更改后接受，您可以在此处监控 PO，直到客户发送新版本。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-118">If you rejected the PO or accepted it with changes, you can monitor the PO here until the customer sends a new version.</span></span>
-   <span data-ttu-id="f5a1b-119">**打开已确认的采购订单** - 此列表包含您的帐户中状态为“**已确认**”的所有 PO。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-119">**Open confirmed purchase orders** - This list contains all the POs for your account that have a status of **Confirmed**.</span></span> <span data-ttu-id="f5a1b-120">PO 上的产品或服务全部收到后，PO 从此列表中消失。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-120">When products or services are fully received against the PO, the PO disappears from the list.</span></span>

<span data-ttu-id="f5a1b-121">以下列表显示了您处理采购订单时可以使用的四个页面，其中两个页面包含与工作区中的列表相同的信息：</span><span class="sxs-lookup"><span data-stu-id="f5a1b-121">The following list shows the four pages that you can use to work with purchase orders, two of which contain the same information as the lists in the workspace:</span></span>

-   <span data-ttu-id="f5a1b-122">**要审核的采购订单**（见上文）</span><span class="sxs-lookup"><span data-stu-id="f5a1b-122">**Purchase orders for review** (see above)</span></span>
-   <span data-ttu-id="f5a1b-123">**采购订单供应商确认历史记录** - 此页包含已经发生给供应商的所有 PO 和 PO 的所有版本，以及供应商已经返回的所有响应。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-123">**Purchase order vendor confirmation history** -This page contains all POs and all versions of POs that have been sent to the vendor, and all the responses that have been returned from the vendor.</span></span>
-   <span data-ttu-id="f5a1b-124">**打开已确认的采购订单**（见上文）</span><span class="sxs-lookup"><span data-stu-id="f5a1b-124">**Open confirmed purchase orders** (see above)</span></span>
-   <span data-ttu-id="f5a1b-125">**所有已确认的采购订单** - 此页包含已确认的所有 PO，包括已经收到产品或服务的 PO。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-125">**All confirmed purchase orders** - This page contains all the POs that have been confirmed, including those where products or services have been received.</span></span> <span data-ttu-id="f5a1b-126">您可以使用此列表监控您可以发送发票的 PO。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-126">You can use this list to monitor which POs you can send invoices for.</span></span>

### <a name="responding-to-purchase-orders"></a><span data-ttu-id="f5a1b-127">响应采购订单</span><span class="sxs-lookup"><span data-stu-id="f5a1b-127">Responding to purchase orders</span></span>

<span data-ttu-id="f5a1b-128">客户发送给您审核的采购订单在**采购订单确认**工作区和**要审核的采购订单**页面可见。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-128">The purchase orders that the customer has sent you to review are visible in the **Purchase order confirmation** workspace and on the **Purchase orders for review** page.</span></span> <span data-ttu-id="f5a1b-129">打开 PO 后，您可以选择接受、拒绝或更改后接受。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-129">After you open a PO, you can choose to accept it, reject it, or accept it with changes.</span></span> <span data-ttu-id="f5a1b-130">可以在 PO 标头或单独的行中添加附件。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-130">There could be attachments on the PO header or on individual lines.</span></span> <span data-ttu-id="f5a1b-131">您也可以在您在 PO 标头或单独行上的响应添加信息。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-131">It's also possible for you to attach information to your response on the PO header or individual lines.</span></span> <span data-ttu-id="f5a1b-132">例如，您可以为某一行建议一种替代物料。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-132">For example, you might suggest a substitute item for one of the lines.</span></span> <span data-ttu-id="f5a1b-133">您可以使用“**预览/打印**”选项预览 PO 和打印成 PDF 文件。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-133">You can preview and print the PO as a PDF file by using the **Preview/Print** option.</span></span> <span data-ttu-id="f5a1b-134">您可以使用“**显示维度**”操作隐藏或显示以下维度列：站点、仓库、颜色、尺寸、样式、配置。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-134">You can hide or show the following dimension columns using the **Display dimensions** action: Site, Warehouse, Color, Size, Style, Configuration.</span></span> <span data-ttu-id="f5a1b-135">如果您使用**更改后接受**选项，您可以接受或拒绝单独的行。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-135">If you use the **Accept with changes** option, you can accept or reject individual lines.</span></span> <span data-ttu-id="f5a1b-136">您也可以对行进行以下更改：</span><span class="sxs-lookup"><span data-stu-id="f5a1b-136">You can also make the following changes to lines:</span></span>

-   <span data-ttu-id="f5a1b-137">更改日期或数量。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-137">Change dates or quantities.</span></span> <span data-ttu-id="f5a1b-138">如果您要更新所有行上的已确认交货日期，则使用 PO 标头上的“**更新交货日期**”选项。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-138">If you want to update the confirmed delivery date on all lines, use the **Update delivery date** option on the PO header.</span></span>
-   <span data-ttu-id="f5a1b-139">拆分不同交货日期或数量的行</span><span class="sxs-lookup"><span data-stu-id="f5a1b-139">Split lines for different delivery dates or quantities</span></span>
-   <span data-ttu-id="f5a1b-140">替换物料。 </span><span class="sxs-lookup"><span data-stu-id="f5a1b-140">Substitute an item.</span></span> <span data-ttu-id="f5a1b-141">为此，请在“**行详细信息**”部分的“**外部**”字段中输入物料描述和您的物料编号。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-141">To do this, enter an item description and your item number in the **External** field in the **Line details** section.</span></span>

<span data-ttu-id="f5a1b-142">您无法更改价格信息或费用，但您可以使用附注建议更改。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-142">You can't change pricing information or charges, but you can make suggestions for changes to these using notes.</span></span> <span data-ttu-id="f5a1b-143">如果您的客户向您发送 PO 的新版本，将有一个版本后缀，表示是先前传递的 PO 的修订版本。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-143">If your customer sends you a new version of a PO, this will have a version suffix to indicate that it’s a modified version of a PO that was previously communicated.</span></span> <span data-ttu-id="f5a1b-144">**采购订单供应商确认历史记录**页允许您跟踪每个订单的历史记录。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-144">The **Purchase order vendor confirmation history** page allows you to track the history of each order.</span></span>

## <a name="monitoring-consignment-inventory"></a><span data-ttu-id="f5a1b-145">监控托运库存</span><span class="sxs-lookup"><span data-stu-id="f5a1b-145">Monitoring consignment inventory</span></span>
<span data-ttu-id="f5a1b-146">如果正在使用托运库存，您可以使用供应商协作界面查看有关以下页面的信息：</span><span class="sxs-lookup"><span data-stu-id="f5a1b-146">If you’re using consignment inventory, you can use the vendor collaboration interface to view information on the following pages:</span></span>

-   <span data-ttu-id="f5a1b-147">**使用托运库存的采购订单** - 客户获得库存的所有权时，生成托运库存的采购订单。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-147">**Purchase orders consuming consignment inventory** - Purchase orders for consignment inventory are generated when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="f5a1b-148">这些托运采购订单仅显示在“**使用托运库存的采购订单**”页面上。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-148">These consignment purchase orders are only displayed on the **Purchase orders consuming consignment inventory** page.</span></span> <span data-ttu-id="f5a1b-149">它们不包括在“**所有已确认的采购订单**”页上。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-149">They are not included on the **All confirmed purchase orders** page.</span></span>
-   <span data-ttu-id="f5a1b-150">**从托运库存接收的产品** - 此页列出产品所有权转移至使用库存的公司的所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-150">**Products received from consignment inventory** - This page lists all the transactions where the ownership of products has been transferred to the company that’s consuming the inventory.</span></span> <span data-ttu-id="f5a1b-151">您可以使用此信息对客户开票。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-151">You can use this information to invoice the customer.</span></span>
-   <span data-ttu-id="f5a1b-152">**现有托运库存** - 此页显示客户仓库现有的您的公司拥有的现有托运库存。</span><span class="sxs-lookup"><span data-stu-id="f5a1b-152">**On-hand consignment inventory** - This page shows the on-hand consignment inventory owned by your company that is on-hand at the customers warehouse.</span></span>


<a name="see-also"></a><span data-ttu-id="f5a1b-153">请参阅</span><span class="sxs-lookup"><span data-stu-id="f5a1b-153">See also</span></span>
--------

[<span data-ttu-id="f5a1b-154">管理供应商协作用户</span><span class="sxs-lookup"><span data-stu-id="f5a1b-154">Manage vendor collaboration users</span></span>](manage-vendor-collaboration-users.md)




