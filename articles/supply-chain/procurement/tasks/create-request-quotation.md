---
title: 创建询价
description: 此过程向您说明如何创建询价。
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchCreateRFQCase, InventLocationIdLookup, PurchRFQCaseTable, InventItemIdLookupSimple, EcoResCategorySingleLookup, UnitOfMeasureLookup, PurchRFQEditLines, PurchRFQEditLinesPrintOptions, VendRFQJournal, SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59202cb6678660ae035f9f76ebe4267bac01d78f
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019896"
---
# <a name="create-a-request-for-quotation"></a><span data-ttu-id="816ec-103">创建询价</span><span class="sxs-lookup"><span data-stu-id="816ec-103">Create a request for quotation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="816ec-104">此过程向您说明如何创建询价。</span><span class="sxs-lookup"><span data-stu-id="816ec-104">This procedure shows you how to create a request for quotation.</span></span> <span data-ttu-id="816ec-105">这通常由采购代理完成。</span><span class="sxs-lookup"><span data-stu-id="816ec-105">This would typically be done by a purchasing agent.</span></span> <span data-ttu-id="816ec-106">您可以使用演示数据公司 USMF，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="816ec-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="816ec-107">在您开始之前，您需要设置申请类型。</span><span class="sxs-lookup"><span data-stu-id="816ec-107">You need to have set up solicitation types before you start.</span></span> <span data-ttu-id="816ec-108">一旦您完成此任务，并且您已创建和发送了询价，然后您可以输入每个供应商的回复，比较它们并授予合同。</span><span class="sxs-lookup"><span data-stu-id="816ec-108">Once you've completed this task and you've created and sent an RFQ you can then enter the replies per vendor, compare them, and award the contract.</span></span>


## <a name="prepare-a-new-rfq"></a><span data-ttu-id="816ec-109">准备新询价</span><span class="sxs-lookup"><span data-stu-id="816ec-109">Prepare a new RFQ</span></span>
1. <span data-ttu-id="816ec-110">转到 **导航窗格 > 模块 > 采购 > 询价 > 所有询价**。</span><span class="sxs-lookup"><span data-stu-id="816ec-110">Go to **Navigation pane > Modules > Procurement and sourcing > Requests for quotations > All requests for quotations**.</span></span>
2. <span data-ttu-id="816ec-111">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="816ec-111">Click **New**.</span></span>
    <span data-ttu-id="816ec-112">提供以下采购类型：采购订单（这是默认值）：确认购买产品的优惠的文档，或对交换付款的产品销售的优惠的接受。</span><span class="sxs-lookup"><span data-stu-id="816ec-112">The following purchase types are available: Purchase order (this is the default): a document that confirms the offer to buy products, or the acceptance of an offer to sell products in exchange for payment.</span></span> <span data-ttu-id="816ec-113">采购申请：如果您直接从采购申请创建一个询价，则此类型将自动选中。</span><span class="sxs-lookup"><span data-stu-id="816ec-113">Purchase requisition: this type is automatically selected if you create an RFQ directly from a purchase requisition.</span></span> <span data-ttu-id="816ec-114">如果您手动选择此选项，您将收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="816ec-114">If you manually select this option, you'll get an error.</span></span> <span data-ttu-id="816ec-115">采购协议：一段时间内采购特定数量或特定价值产品的协议。</span><span class="sxs-lookup"><span data-stu-id="816ec-115">Purchase agreement: an agreement to purchase a specific quantity or value of product over time.</span></span> <span data-ttu-id="816ec-116">如果您选择此选项，则必须选择适用于采购协议的日期范围。</span><span class="sxs-lookup"><span data-stu-id="816ec-116">If you select this option, you must select the date range that applies to the purchase agreement.</span></span>  
3. <span data-ttu-id="816ec-117">在 **文档标题** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="816ec-117">In the **Document title** field, type a value.</span></span>
4. <span data-ttu-id="816ec-118">在 **申请类型** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="816ec-118">In the **Solicitation type** field, enter or select a value.</span></span>
    + <span data-ttu-id="816ec-119">如果计分方法与申请类型关联，这将是您创建的 RFQ 的默认计分方法。</span><span class="sxs-lookup"><span data-stu-id="816ec-119">If a scoring method is associated with the solicitation type, this will be the default scoring method for the RFQ that you're creating.</span></span> <span data-ttu-id="816ec-120">以后可以更改计分方法。</span><span class="sxs-lookup"><span data-stu-id="816ec-120">It is possible to change the scoring method later.</span></span>  
    + <span data-ttu-id="816ec-121">在 **交货日期** 字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="816ec-121">In the **Delivery date** field, enter a date.</span></span>  
    + <span data-ttu-id="816ec-122">选择您要接收物料的最晚日期。</span><span class="sxs-lookup"><span data-stu-id="816ec-122">Select the date by which you want to receive the items.</span></span>  
    + <span data-ttu-id="816ec-123">在 **到期日期和时间** 字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="816ec-123">In the **Expiration date and time** field, enter a date and time.</span></span>  
    + <span data-ttu-id="816ec-124">指定供应商必须响应 RFQ 的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="816ec-124">Specify the date and time by which vendors must respond to the RFQ.</span></span>  
5. <span data-ttu-id="816ec-125">在 **仓库** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="816ec-125">In the **Warehouse field**, enter or select a value.</span></span> <span data-ttu-id="816ec-126">交货地址将默认为仓库地址。</span><span class="sxs-lookup"><span data-stu-id="816ec-126">The delivery address will default to the warehouse address.</span></span>  
6. <span data-ttu-id="816ec-127">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="816ec-127">Click **OK**.</span></span>

## <a name="add-lines"></a><span data-ttu-id="816ec-128">添加多行</span><span class="sxs-lookup"><span data-stu-id="816ec-128">Add lines</span></span>

<span data-ttu-id="816ec-129">在 RFQ 中指定基本信息后，请指定希望供应商出价的货物或服务。</span><span class="sxs-lookup"><span data-stu-id="816ec-129">After you've specified the basic information about your RFQ, you specify the goods or services that you want vendors to bid on.</span></span> <span data-ttu-id="816ec-130">物料是默认的行类型。</span><span class="sxs-lookup"><span data-stu-id="816ec-130">Item is the default line type.</span></span>

1. <span data-ttu-id="816ec-131">在 **物料编号** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="816ec-131">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="816ec-132">如果您正在使用 USMF，可以选择 T0020。</span><span class="sxs-lookup"><span data-stu-id="816ec-132">If you're using USMF, you can select T0020.</span></span>  
2. <span data-ttu-id="816ec-133">在 **数量** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="816ec-133">In the **Quantity** field, enter a number.</span></span>
3. <span data-ttu-id="816ec-134">单击 **添加行**。</span><span class="sxs-lookup"><span data-stu-id="816ec-134">Click **Add line**.</span></span>
4. <span data-ttu-id="816ec-135">在 **行类型** 字段中选择“类别”。</span><span class="sxs-lookup"><span data-stu-id="816ec-135">In the **Line type** field, select 'Category'.</span></span> <span data-ttu-id="816ec-136">您可以使用类别行类型类别创建非库存货物或服务的询价。</span><span class="sxs-lookup"><span data-stu-id="816ec-136">You can use the Category line type to create RFQs for non-inventory goods or services.</span></span> <span data-ttu-id="816ec-137">您将需要从采购类别层次结构中选择货物或服务的类型。</span><span class="sxs-lookup"><span data-stu-id="816ec-137">You then need to select the type of goods or services from a hierarchy of procurement categories.</span></span>  
5. <span data-ttu-id="816ec-138">在 **采购类别** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="816ec-138">In the **Procurement category** field, enter or select a value.</span></span>
6. <span data-ttu-id="816ec-139">在 **产品名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="816ec-139">In the **Product name** field, type a value.</span></span>
7. <span data-ttu-id="816ec-140">在 **数量** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="816ec-140">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="816ec-141">在 **单位** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="816ec-141">In the **Unit** field, enter or select a value.</span></span>

## <a name="add-vendors"></a><span data-ttu-id="816ec-142">添加供应商</span><span class="sxs-lookup"><span data-stu-id="816ec-142">Add vendors</span></span>
1. <span data-ttu-id="816ec-143">单击 **标题** 将行视图更改为标题视图。</span><span class="sxs-lookup"><span data-stu-id="816ec-143">Click **Header** to change from the Lines view to the Header view.</span></span> 
2. <span data-ttu-id="816ec-144">展开 **供货商** 部分。</span><span class="sxs-lookup"><span data-stu-id="816ec-144">Expand the **Vendor** section.</span></span>
3. <span data-ttu-id="816ec-145">单击 **自动添加供应商**。</span><span class="sxs-lookup"><span data-stu-id="816ec-145">Click **Auto-add vendors**.</span></span> <span data-ttu-id="816ec-146">您可以基于请求物料的采购类别，自动添加供应商到 RFQ。</span><span class="sxs-lookup"><span data-stu-id="816ec-146">You can add vendors to the RFQ automatically, based on the procurement category of the items requested.</span></span> <span data-ttu-id="816ec-147">如果没有包括在行中的类别的通过审批的供应商，您可以手动添加供应商。</span><span class="sxs-lookup"><span data-stu-id="816ec-147">If there are no vendors approved for the categories included in the lines you can add vendors manually.</span></span>  
4. <span data-ttu-id="816ec-148">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="816ec-148">Click **Add**.</span></span>
5. <span data-ttu-id="816ec-149">在 **供应商帐户** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="816ec-149">In the **Vendor account** field, enter or select a value.</span></span>
6. <span data-ttu-id="816ec-150">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="816ec-150">Click **Add**.</span></span>
7. <span data-ttu-id="816ec-151">在 **供应商帐户** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="816ec-151">In the **Vendor account** field, enter or select a value.</span></span> <span data-ttu-id="816ec-152">一旦选择了供应商，状态将为“已创建”。</span><span class="sxs-lookup"><span data-stu-id="816ec-152">Once you've selected a vendor, the status is Created.</span></span> <span data-ttu-id="816ec-153">这意味着供应商信息已保存在询价中，但您尚未发送该询价给供应商。</span><span class="sxs-lookup"><span data-stu-id="816ec-153">This means that the vendor information has been saved in the RFQ, but you have not sent the RFQ to the vendor.</span></span> <span data-ttu-id="816ec-154">无论供应商状态为何，您可以将供应商添加到询价。</span><span class="sxs-lookup"><span data-stu-id="816ec-154">You can add a vendor to an RFQ regardless of the vendor status.</span></span>  

## <a name="send-the-rfq-to-vendors"></a><span data-ttu-id="816ec-155">将 RFQ 发送给供应商</span><span class="sxs-lookup"><span data-stu-id="816ec-155">Send the RFQ to vendors</span></span>
1. <span data-ttu-id="816ec-156">在 **操作窗格** 上，单击 **发送**。</span><span class="sxs-lookup"><span data-stu-id="816ec-156">On the **Action Pane**, click **Send**.</span></span> <span data-ttu-id="816ec-157">在发送询价页面，检查列表中的供应商是您要接收询价的供应商。</span><span class="sxs-lookup"><span data-stu-id="816ec-157">In the Sending request for quotation page, check that the vendors in the list are the ones that you want to receive the RFQ.</span></span>  
2. <span data-ttu-id="816ec-158">单击 **打印**。</span><span class="sxs-lookup"><span data-stu-id="816ec-158">Click **Print**.</span></span> <span data-ttu-id="816ec-159">此对话框允许您打印询价。</span><span class="sxs-lookup"><span data-stu-id="816ec-159">This dialog allows you to print the RFQ.</span></span> <span data-ttu-id="816ec-160">如果您选择打印回复表，此字段的内容在采购参数中定义。</span><span class="sxs-lookup"><span data-stu-id="816ec-160">If you choose to print a reply sheet, the contents of this are defined in Procurement and Sourcing parameters.</span></span> <span data-ttu-id="816ec-161">若要选择如何打印回复表，在您开始打印对话框后，单击高级打印选项。</span><span class="sxs-lookup"><span data-stu-id="816ec-161">To choose how to print reply sheets, once you've opened the Print dialog, click Advanced printing options.</span></span> <span data-ttu-id="816ec-162">将为包含具有状态“已创建”或“已发送”的行的每个供应商打印一个询价。</span><span class="sxs-lookup"><span data-stu-id="816ec-162">One RFQ will be printed for each vendor containing the lines that have the status of Created or Sent.</span></span> <span data-ttu-id="816ec-163">已取消的行以及具有已登记回复的行将不打印。</span><span class="sxs-lookup"><span data-stu-id="816ec-163">Canceled lines and lines with registered replies will not be printed.</span></span>   
3. <span data-ttu-id="816ec-164">单击 **取消**。</span><span class="sxs-lookup"><span data-stu-id="816ec-164">Click **Cancel**.</span></span>
4. <span data-ttu-id="816ec-165">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="816ec-165">Click **OK**.</span></span>
5. <span data-ttu-id="816ec-166">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="816ec-166">Close the page.</span></span>
6. <span data-ttu-id="816ec-167">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="816ec-167">Close the page.</span></span>

## <a name="view-the-rfq-journal"></a><span data-ttu-id="816ec-168">查看询价日记帐。</span><span class="sxs-lookup"><span data-stu-id="816ec-168">View the RFQ journal</span></span>
1. <span data-ttu-id="816ec-169">转到 **采购 > 询价 > 询价跟进 > 报价单日记帐**。</span><span class="sxs-lookup"><span data-stu-id="816ec-169">Go to **Procurement and sourcing > Requests for quotations > Request for quotations follow-up > Request for quotation journals**.</span></span>
2. <span data-ttu-id="816ec-170">单击 **预览/打印**。</span><span class="sxs-lookup"><span data-stu-id="816ec-170">Click **Preview/Print**.</span></span>
3. <span data-ttu-id="816ec-171">单击 **原件预览**。</span><span class="sxs-lookup"><span data-stu-id="816ec-171">Click **Original preview**.</span></span>
4. <span data-ttu-id="816ec-172">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="816ec-172">Close the page.</span></span>
5. <span data-ttu-id="816ec-173">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="816ec-173">Close the page.</span></span>

