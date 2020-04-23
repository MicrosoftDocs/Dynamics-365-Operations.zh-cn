---
title: 供应商与客户的协作
description: 本主题介绍您如何使用供应商协作处理采购订单和监控托运库存。
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 240fdfb3519e1c4526c46fa3d5e3fbaa8e5a467e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207339"
---
# <a name="vendor-collaboration-with-customers"></a><span data-ttu-id="c7ab2-103">供应商与客户的协作</span><span class="sxs-lookup"><span data-stu-id="c7ab2-103">Vendor collaboration with customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7ab2-104">本主题介绍您在 Microsoft Dynamics 365 Supply Chain Management 中如何使用供应商协作处理客户。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-104">This topic describes how you can use vendor collaboration to work with customers in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c7ab2-105">供应商可以从以下工作区完成一系列业务流程：</span><span class="sxs-lookup"><span data-stu-id="c7ab2-105">Vendors can complete a series of business processes from the following workspaces:</span></span>

- <span data-ttu-id="c7ab2-106">**采购订单确认** - 监视和响应采购订单 (PO)。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-106">**Purchase order confirmation** – Monitor and respond to purchase orders (POs).</span></span>
- <span data-ttu-id="c7ab2-107">**供应商出价** - 查看询价 (RFQ) 并输入出价以响应询价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-107">**Vendor bidding** – View requests for quotation (RFQs), and respond to them by entering bids.</span></span>
- <span data-ttu-id="c7ab2-108">**供应商信息** - 查看和更新供应商主数据。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-108">**Vendor information** – View and update vendor master data.</span></span>
- <span data-ttu-id="c7ab2-109">**开票** - 处理发票。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-109">**Invoicing** – Work with invoices.</span></span> <span data-ttu-id="c7ab2-110">此主题不包括**开票**工作区。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-110">This topic doesn't cover the **Invoicing** workspace.</span></span> <span data-ttu-id="c7ab2-111">有关此工作区的详细信息，请参阅[供应商协作开票工作区](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md)。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-111">For more information about this workspace, see [Vendor collaboration invoicing workspace](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md).</span></span>

<span data-ttu-id="c7ab2-112">供应商还可以监视与托运库存有关的信息。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-112">Vendors can also monitor information about consignment inventory.</span></span>

## <a name="working-with-pos-in-the-purchase-order-confirmation-workspace"></a><span data-ttu-id="c7ab2-113">在“采购订单确认”工作区处理 PO</span><span class="sxs-lookup"><span data-stu-id="c7ab2-113">Working with POs in the Purchase order confirmation workspace</span></span>

<span data-ttu-id="c7ab2-114">**采购订单确认**工作区允许您响应发送给您审核的采购订单。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-114">The **Purchase order confirmation** workspace lets you respond to the POs that have been sent to you for review.</span></span> <span data-ttu-id="c7ab2-115">您还可以查看正在等待客户操作的采购订单的信息，以及已确认但仍然未结的采购订单的信息。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-115">It also lets you view information about POs that are awaiting action from the customer, and POs that have been confirmed but are still open.</span></span>

<span data-ttu-id="c7ab2-116">**采购订单确认**工作区有三个列表：</span><span class="sxs-lookup"><span data-stu-id="c7ab2-116">There are three lists in the **Purchase order confirmation** workspace:</span></span>

- <span data-ttu-id="c7ab2-117">**要审核的采购订单** - 此列表显示已经发送给您并且正在等待您响应的采购订单。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-117">**Purchase orders for review** – This list shows POs that have been sent to you and are awaiting a response from you.</span></span> <span data-ttu-id="c7ab2-118">您做出响应后，采购订单将从列表中消失。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-118">After you respond, the PO disappears from the list.</span></span> <span data-ttu-id="c7ab2-119">如果在您响应之前的采购订单版本之前，客户向您发送了采购订单的新版本，则仅显示最新版本。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-119">If the customer sends you a new version of the PO before you've responded to the previous version, only the latest version is shown.</span></span>
- <span data-ttu-id="c7ab2-120">**正在等待客户操作** - 此列表显示您已经响应，但客户尚未确认的所有采购订单。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-120">**Awaiting customer action** – This list shows all the POs that you've responded to but that the customer hasn't yet confirmed.</span></span> <span data-ttu-id="c7ab2-121">如果您接受了 PO，您可以在此列表中进行监控，直到状态更改为**已确认**。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-121">If you accept a PO, you can monitor it in this list until the status is changed to **Confirmed**.</span></span> <span data-ttu-id="c7ab2-122">如果您拒绝 PO 或更改后接受，您可以在此处监控它，直到客户发送新版本。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-122">If you reject a PO or accept it with changes, you can monitor it here until the customer sends a new version.</span></span>
- <span data-ttu-id="c7ab2-123">**打开已确认的采购订单** - 此列表显示您的帐户中状态为**已确认**的所有 PO。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-123">**Open confirmed purchase orders** – This list shows all the POs for your account that have a status of **Confirmed**.</span></span> <span data-ttu-id="c7ab2-124">PO 上的产品或服务全部收到后，PO 从此列表中消失。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-124">When products or services are fully received against the PO, the PO disappears from the list.</span></span>

<span data-ttu-id="c7ab2-125">您可以使用以下页面处理 PO：</span><span class="sxs-lookup"><span data-stu-id="c7ab2-125">You can use the following pages to work with POs:</span></span>

- <span data-ttu-id="c7ab2-126">**要审核的采购订单** - 此页包含的信息与工作区中的**要审核的采购订单**包含的信息相同。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-126">**Purchase orders for review** – This page contains the same information as the **Purchase orders for review** list in the workspace.</span></span> <span data-ttu-id="c7ab2-127">请参阅本主题前文描述。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-127">See the description earlier in this topic.</span></span>
- <span data-ttu-id="c7ab2-128">**采购订单供应商确认历史记录** - 此页包含已发送给供应商的所有 PO 和 PO 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-128">**Purchase order vendor confirmation history** – This page contains all POs and all versions of POs that have been sent to the vendor.</span></span> <span data-ttu-id="c7ab2-129">它还包含来自供应商返回的所有响应。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-129">It also contains all the responses that have been returned from the vendor.</span></span>
- <span data-ttu-id="c7ab2-130">**打开已确认的采购订单**此页包含的信息与工作区中的**打开已确认的采购订单**包含的信息相同。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-130">**Open confirmed purchase orders** This page contains the same information as the **Open confirmed purchase order** list in the workspace.</span></span> <span data-ttu-id="c7ab2-131">请参阅本主题前文描述。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-131">See the description earlier in this topic.</span></span>
- <span data-ttu-id="c7ab2-132">**所有已确认的采购订单** - 此页包含所有已确认的 PO。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-132">**All confirmed purchase orders** – This page contains all the POs that have been confirmed.</span></span> <span data-ttu-id="c7ab2-133">此页上的 PO 包括已经收到产品或服务的 PO。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-133">The POs on this page include POs where products or services have been received.</span></span> <span data-ttu-id="c7ab2-134">您可以使用此列表监控您可以发送发票的 PO。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-134">You can use this list to monitor POs that you can send invoices for.</span></span>

### <a name="responding-to-pos"></a><span data-ttu-id="c7ab2-135">响应 PO</span><span class="sxs-lookup"><span data-stu-id="c7ab2-135">Responding to POs</span></span>

<span data-ttu-id="c7ab2-136">客户发送给您审核的采购订单显示在**采购订单确认**工作区和**要审核的采购订单**页上。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-136">The POs that the customer sends you to review appear in the **Purchase order confirmation** workspace and on the **Purchase orders for review** page.</span></span> <span data-ttu-id="c7ab2-137">打开 PO 后，您可以接受、拒绝或更改后接受。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-137">After you open a PO, you can accept it, reject it, or accept it with changes.</span></span> <span data-ttu-id="c7ab2-138">可以在 PO 标头或单独的行中添加附件。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-138">There might be attachments on the PO header or on individual lines.</span></span> <span data-ttu-id="c7ab2-139">您也可以对您在 PO 标头或单独行上的响应添加信息。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-139">Additionally, you can attach information to your response on the PO header or individual lines.</span></span> <span data-ttu-id="c7ab2-140">例如，您可以为某一行建议一种替代物料。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-140">For example, you might suggest a substitute item for one of the lines.</span></span>

<span data-ttu-id="c7ab2-141">您可以使用**预览/打印**选项预览 PO 和打印成 PDF 文件。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-141">You can preview and print the PO as a PDF file by using the **Preview/Print** option.</span></span> <span data-ttu-id="c7ab2-142">您可以使用**显示维度**操作隐藏或显示以下维度列：**站点**、**仓库**、**颜色**、**尺寸**、**样式**和**配置**。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-142">You can also use the **Display dimensions** action to hide or show the following dimension columns: **Site**, **Warehouse**, **Color**, **Size**, **Style**, and **Configuration**.</span></span> 

<span data-ttu-id="c7ab2-143">如果您使用**更改后接受**选项，您可以接受或拒绝单独的行。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-143">If you use the **Accept with changes** option, you can accept or reject individual lines.</span></span> <span data-ttu-id="c7ab2-144">您也可以对行进行以下更改：</span><span class="sxs-lookup"><span data-stu-id="c7ab2-144">You can also make the following changes to lines:</span></span>

- <span data-ttu-id="c7ab2-145">更改日期或数量。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-145">Change dates or quantities.</span></span> <span data-ttu-id="c7ab2-146">若要更新所有行上的已确认交货日期，则使用 PO 标头上的**更新交货日期**选项。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-146">To update the confirmed delivery date on all lines, use the **Update delivery date** option on the PO header.</span></span>
- <span data-ttu-id="c7ab2-147">拆分不同交货日期或数量的行。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-147">Split lines for different delivery dates or quantities.</span></span>
- <span data-ttu-id="c7ab2-148">替换物料。 </span><span class="sxs-lookup"><span data-stu-id="c7ab2-148">Substitute an item.</span></span> <span data-ttu-id="c7ab2-149">在**行明细**部分的**外部**字段中输入物料描述和物料编号。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-149">In the **Line details** section, enter an item description and the item number in the **External** field.</span></span>

<span data-ttu-id="c7ab2-150">您无法更改价格信息或费用，但可以使用注释建议更改。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-150">You can't change pricing information or charges, but you can use notes to make suggestions for these changes.</span></span>

<span data-ttu-id="c7ab2-151">如果客户向您发送 PO 的新版本，将有一个版本后缀，表示是先前发送的 PO 的修订版本。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-151">If the customer sends you a new version of a PO, it will have a version suffix to indicate that it's a modified version of a PO that was previously sent.</span></span> <span data-ttu-id="c7ab2-152">**采购订单供应商确认历史记录**页允许您跟踪每个订单的历史记录。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-152">The **Purchase order vendor confirmation history** page lets you track the history of each order.</span></span>

## <a name="monitoring-consignment-inventory"></a><span data-ttu-id="c7ab2-153">监控托运库存</span><span class="sxs-lookup"><span data-stu-id="c7ab2-153">Monitoring consignment inventory</span></span>

<span data-ttu-id="c7ab2-154">如果正在使用托运库存，您可以使用供应商协作界面查看有关以下页面的信息：</span><span class="sxs-lookup"><span data-stu-id="c7ab2-154">If you're using consignment inventory, you can use the vendor collaboration interface to view information on the following pages:</span></span>

- <span data-ttu-id="c7ab2-155">**使用托运库存的采购订单** - 客户获得库存的所有权时，生成托运库存的 PO。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-155">**Purchase orders consuming consignment inventory** – POs for consignment inventory are generated when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="c7ab2-156">这些托运 PO 仅显示在此页上。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-156">These consignment POs are shown only on this page.</span></span> <span data-ttu-id="c7ab2-157">它们不包括在**所有已确认的采购订单**页上。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-157">They aren't included on the **All confirmed purchase orders** page.</span></span>
- <span data-ttu-id="c7ab2-158">**从托运库存接收的产品** - 此页列出产品所有权转移至使用库存的公司的所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-158">**Products received from consignment inventory** – This page lists all the transactions where the ownership of products has been transferred to the company that is consuming the inventory.</span></span> <span data-ttu-id="c7ab2-159">您可以使用此信息对客户开票。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-159">You can use this information to invoice the customer.</span></span>
- <span data-ttu-id="c7ab2-160">**现有托运库存** - 此页显示您的公司拥有，但在客户仓库现有的现有托运库存。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-160">**On-hand consignment inventory** – This page shows the on-hand consignment inventory that is owned by your company, but that is on hand at the customer's warehouse.</span></span>

## <a name="working-with-rfqs-in-the-vendor-bidding-workspace"></a><span data-ttu-id="c7ab2-161">在“供应商出价”工作区处理询价</span><span class="sxs-lookup"><span data-stu-id="c7ab2-161">Working with RFQs in the Vendor bidding workspace</span></span>

<span data-ttu-id="c7ab2-162">在**供应商出价**工作区可以查看公司受邀响应的询价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-162">The **Vendor bidding** workspace lets you view the RFQs that your company has been invited to respond to.</span></span> <span data-ttu-id="c7ab2-163">还可以响应询价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-163">You can also respond to the RFQs.</span></span> 

<span data-ttu-id="c7ab2-164">该工作区还显示您已经失去或赢得的所有询价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-164">The workspace also shows all the RFQs that you've lost or won.</span></span> <span data-ttu-id="c7ab2-165">此外，如果针对公共部门配置了该系统，该工作区将显示公开可用的询价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-165">Additionally, if the system is configured for the Public sector, the workspace shows the RFQs that are publicly available.</span></span>

### <a name="viewing-rfqs"></a><span data-ttu-id="c7ab2-166">查看询价</span><span class="sxs-lookup"><span data-stu-id="c7ab2-166">Viewing RFQs</span></span>

<span data-ttu-id="c7ab2-167">打开**供应商出价**工作区以访问以下信息：</span><span class="sxs-lookup"><span data-stu-id="c7ab2-167">Open the **Vendor bidding** workspace to access the following information:</span></span>

- <span data-ttu-id="c7ab2-168">选择**新出价邀请**以查看您的公司受邀响应的询价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-168">Select **New bid invitations** to see the RFQs that your company has been invited to respond to.</span></span> <span data-ttu-id="c7ab2-169">在此处可以查看询价并启动投标过程。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-169">From here, you can view an RFQ and start the bidding process.</span></span> <span data-ttu-id="c7ab2-170">您还可以查看必须提交新出价的改正后的询价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-170">You can also see amended RFQs that a new bid must be submitted for.</span></span>
- <span data-ttu-id="c7ab2-171">选择**返回出价**以查看客户返回给您的询价，以便您可以提供更多信息或更新出价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-171">Select **Returned bids** to see the RFQs that the customer has returned to you so that you can provide more information or update the bid.</span></span>
- <span data-ttu-id="c7ab2-172">选择**进行中的出价**以查看您或代表您公司的联系人已经开始处理但尚未提交的询价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-172">Select **Bids in progress** to see the RFQs that you or a contact person who represents your company has been working on but hasn't yet submitted.</span></span>
- <span data-ttu-id="c7ab2-173">选择**已分配的出价**以查看客户何时在您的出价中分配了至少一个行项。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-173">Select **Awarded bids** to see when the customer has awarded at least one line item in your bid.</span></span>
- <span data-ttu-id="c7ab2-174">选择**出价失败**以查看所有行被拒绝的出价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-174">Select **Lost bids** to see bids where all lines have been rejected.</span></span>
- <span data-ttu-id="c7ab2-175">选择**询价**链接以查看供应商的所有询价邀请以及已经提交的所有出价的列表。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-175">Select the **Request for quotations** link to see a list of all the vendor's RFQ invitations and any bids that have been submitted.</span></span> <span data-ttu-id="c7ab2-176">**询价**页列出了供应商已经参与的所有询价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-176">The **Request for quotations** page lists all the RFQs that a vendor has been involved in.</span></span> <span data-ttu-id="c7ab2-177">可以按状态搜索。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-177">You can search by status.</span></span>
- <span data-ttu-id="c7ab2-178">选择**已被否决的出价**链接可以查看供应商的联系人已经拒绝出价的所有询价的列表。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-178">Select the **Declined bids** link to see a list of all the RFQs where a vendor's contact person has declined to bid.</span></span>

### <a name="working-with-rfqs-that-are-publicly-available"></a><span data-ttu-id="c7ab2-179">处理公开提供的询价</span><span class="sxs-lookup"><span data-stu-id="c7ab2-179">Working with RFQs that are publicly available</span></span>

<span data-ttu-id="c7ab2-180">公共部门的工作人员可以查看已经公开提供的开放的已到期询价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-180">People who work in the Public sector can see open and expired RFQs that have been made available to the public.</span></span>

- <span data-ttu-id="c7ab2-181">选择**打开发布的询价**链接可以查看公开提供的开放询价的列表。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-181">Select the **Open published requests for quotations** link to see a list of open RFQs that are available to the public.</span></span> <span data-ttu-id="c7ab2-182">开放的询价是指尚未到期的询价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-182">An open RFQ is an RFQ that hasn't yet expired.</span></span> <span data-ttu-id="c7ab2-183">在询价标头上可以找到到期日期和时间。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-183">You can find the expiration date and time on the header of the RFQ.</span></span>

    <span data-ttu-id="c7ab2-184">如果您收到了出价邀请，在**新出价邀请**页上可以找到相同的询价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-184">If you've been invited to bid, you can find the same RFQ on the **New bid invitations** page.</span></span> <span data-ttu-id="c7ab2-185">在某些情况下，您可能要对您未收到出价邀请的开放询价出价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-185">Sometimes, you might want to bid on an open RFQ, but you haven't been invited to bid.</span></span> <span data-ttu-id="c7ab2-186">在这种情况下，您可能可以邀请您自己，前提是客户已经对该询价案例启用了自行邀请。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-186">In this case, you might be able to invite yourself, provided that the customer has enabled self-invitation for the RFQ case.</span></span>

- <span data-ttu-id="c7ab2-187">选择**关闭的已发布询价**链接可以查看公开提供的已关闭询价的列表。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-187">Select the **Closed published requests for quotations** link to see a list of closed RFQs that are available to the public.</span></span> <span data-ttu-id="c7ab2-188">关闭的询价是已经到期的询价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-188">A closed RFQ is an RFQ that has expired.</span></span> <span data-ttu-id="c7ab2-189">在询价标头上可以找到到期日期和时间。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-189">You can find the expiration date and time on the header of the RFQ.</span></span>

    <span data-ttu-id="c7ab2-190">关闭的询价显示下至行级别的所有供应商出价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-190">A closed RFQ shows all vendor bids down to the line level.</span></span> <span data-ttu-id="c7ab2-191">出价被分配或拒绝后，此信息反映在关闭的询价中。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-191">As bids are awarded or rejected, this information is reflected in the closed RFQ.</span></span> <span data-ttu-id="c7ab2-192">出价中包括的任何附件也可用。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-192">Any attachments that are included in the bid are also available.</span></span>

<span data-ttu-id="c7ab2-193">**注意：** 此功能仅在启用了公共部门配置时可用。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-193">**Note:** This functionality is only available if the Public sector cofiguration is enabled.</span></span>

### <a name="bidding"></a><span data-ttu-id="c7ab2-194">出价</span><span class="sxs-lookup"><span data-stu-id="c7ab2-194">Bidding</span></span>

- <span data-ttu-id="c7ab2-195">单击**出价**可以开始对询价出价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-195">Click **Bid** to start to bid on an RFQ.</span></span>

    <span data-ttu-id="c7ab2-196">对询价的标头和行上的出价字段启用编辑后，可以直接在行网格中输入出价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-196">When the editing is enabled for bid fields on the headers and lines of an RFQ, you can enter your bid directly in the line grid.</span></span> <span data-ttu-id="c7ab2-197">您还必须考虑应该添加在行明细中的任何额外的出价信息。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-197">You must also consider any additional bid information that should be added in the line details.</span></span>

    <span data-ttu-id="c7ab2-198">开始处理出价后，出价显示在**进行中的出价**部分。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-198">When you start to work on a bid, it appears in the **Bids in progress** section.</span></span>

    <span data-ttu-id="c7ab2-199">在到期日期之前的任何时候都可以保存出价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-199">At any time before the expiration date, you can save a bid.</span></span> <span data-ttu-id="c7ab2-200">以后再回来完成并提交出价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-200">You can then return later to finish and submit the bid.</span></span> <span data-ttu-id="c7ab2-201">提交出价后，在到期日期前可以撤回和更新出价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-201">After you submit a bid, you can recall and update it up until the expiration date.</span></span>

- <span data-ttu-id="c7ab2-202">选择**重设询价**可以重置为出价输入的数据和恢复为原始询价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-202">Select **Reset from RFQ** to reset the data that you entered for a bid and revert to the original RFQ.</span></span> <span data-ttu-id="c7ab2-203">您可以重置标头或行。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-203">You can reset the header or the line.</span></span>
- <span data-ttu-id="c7ab2-204">选择行网格中的**添加备选**或**删除备选**可以处理备选。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-204">Select **Add alternate** or **Remove alternate** in the line grid to work with alternates.</span></span>

    <span data-ttu-id="c7ab2-205">一些询价允许备选出价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-205">Some RFQs allow for alternate bids.</span></span> <span data-ttu-id="c7ab2-206">您只能对**类别**类型的行指定备选出价，因为特定项不能作为备选添加。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-206">You can specify alternate bids only for lines of the **Category** type, because specific items can't be added as alternates.</span></span> 

- <span data-ttu-id="c7ab2-207">选择**询价附件**或**询价行附件**可以打开客户添加到询价的任何附件。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-207">Select **RFQ attachment** or **RFQ lines attachment** to open any attachment that the customer has added to an RFQ.</span></span> <span data-ttu-id="c7ab2-208">选择**出价附件**或**出价行附件**可以将附件与出价一起上载。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-208">Select **Bid attachments** or **Bid line attachments** to upload attachments together with the bid.</span></span>

    <span data-ttu-id="c7ab2-209">在允许您提交出价前，您可能必须回答调查表。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-209">There might be questionnaires that you must answer before you're allowed to submit a bid.</span></span>

- <span data-ttu-id="c7ab2-210">如果您不想出价，请选择**拒绝**。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-210">Select **Decline** if you don't want to bid.</span></span> <span data-ttu-id="c7ab2-211">选择**拒绝**后，将无法撤回该操作和输入出价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-211">After you select **Decline**, you can't recall the action and enter a bid.</span></span>

<span data-ttu-id="c7ab2-212">如果改正询价，必须输入新的出价。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-212">If an RFQ is amended, you must enter a new bid.</span></span> <span data-ttu-id="c7ab2-213">在询价页的**改正**选项卡上可以找到有关改正的信息。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-213">You can find information about the amendment on the **Amendments** tab of the RFQ page.</span></span> <span data-ttu-id="c7ab2-214">改正后的询价显示在**新出价邀请**页上。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-214">Amended RFQs appear on the **New bid invitations** page.</span></span>

## <a name="accessing-vendor-master-data-in-the-vendor-information-workspace"></a><span data-ttu-id="c7ab2-215">访问供应商信息工作区中的供应商主数据</span><span class="sxs-lookup"><span data-stu-id="c7ab2-215">Accessing vendor master data in the Vendor information workspace</span></span>

<span data-ttu-id="c7ab2-216">作为供应商，您可以访问客户在供应商主记录中维护的一部分信息。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-216">As a vendor, you can access part of the information that the customer maintains in the vendor master record.</span></span> <span data-ttu-id="c7ab2-217">因此您可以保持最新信息。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-217">Therefore, you can keep the information up to date.</span></span> <span data-ttu-id="c7ab2-218">若要更新信息，必须具有供应商管理员（外部）角色。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-218">To update the information, you must have a vendor admin (external) role.</span></span>

<span data-ttu-id="c7ab2-219">可以访问的信息为供应商名称、地址、联系信息、联系人及其联系信息、身份证明号码、税务登记编号、允许供应商出售给客户的采购类别以及与认证有关的信息。</span><span class="sxs-lookup"><span data-stu-id="c7ab2-219">The accessible information is the vendor name, addresses, contact information, contact persons and their contact information, identification numbers, tax registration numbers, procurement categories that the vendor is approved to sell to the customer in, and information about certifications.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7ab2-220">其他资源</span><span class="sxs-lookup"><span data-stu-id="c7ab2-220">Additional resources</span></span>

[<span data-ttu-id="c7ab2-221">管理供应商协作用户</span><span class="sxs-lookup"><span data-stu-id="c7ab2-221">Manage vendor collaboration users</span></span>](manage-vendor-collaboration-users.md)
