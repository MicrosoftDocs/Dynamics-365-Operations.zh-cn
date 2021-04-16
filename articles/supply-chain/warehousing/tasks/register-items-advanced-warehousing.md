---
title: 使用物料到达日记帐登记启用了高级仓库的物料
description: 本主题提供的场景显示在使用高级仓库管理流程时如何使用物料到达日记帐登记物料。
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c58aa1cec6c0bfe33fa1ef90267dcd8ac1218157
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830826"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="58440-103">使用物料到达日记帐登记启用了高级仓库的物料</span><span class="sxs-lookup"><span data-stu-id="58440-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="58440-104">本主题提供的场景显示在使用高级仓库管理流程时如何使用物料到达日记帐登记物料。</span><span class="sxs-lookup"><span data-stu-id="58440-104">This topic presents a scenario that shows how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="58440-105">这将通常由一个收料员完成。</span><span class="sxs-lookup"><span data-stu-id="58440-105">This would usually be done by a receiving clerk.</span></span>

## <a name="enable-sample-data"></a><span data-ttu-id="58440-106">启用示例数据</span><span class="sxs-lookup"><span data-stu-id="58440-106">Enable sample data</span></span>

<span data-ttu-id="58440-107">若要使用在本主题中指定的示例记录和值完成此场景，您必须使用安装了标准演示数据的系统，并且必须在开始之前选择 *USMF* 法人。</span><span class="sxs-lookup"><span data-stu-id="58440-107">To work through this scenario using the sample records and values specified in this topic, you must be using a system where the standard demo data is installed, and you must select the *USMF* legal entity before you begin.</span></span>

<span data-ttu-id="58440-108">相反，如果您拥有以下可用数据，则可以通过从自己的数据中替换值来完成此场景：</span><span class="sxs-lookup"><span data-stu-id="58440-108">You can instead work through this scenario by substituting values from your own data provided that you have the following data available:</span></span>

- <span data-ttu-id="58440-109">您必须具有包含未结采购订单行的已确认采购订单。</span><span class="sxs-lookup"><span data-stu-id="58440-109">You must have a confirmed purchase order with an open purchase order line.</span></span>
- <span data-ttu-id="58440-110">必须贮存行中的物料。</span><span class="sxs-lookup"><span data-stu-id="58440-110">The item on the line must be stocked.</span></span> <span data-ttu-id="58440-111">它不得使用产品变体，也不得具有跟踪维度。</span><span class="sxs-lookup"><span data-stu-id="58440-111">It must not use product variants, and must not have tracking dimensions.</span></span>
- <span data-ttu-id="58440-112">该物料必须与启用了仓库管理流程的存储维度组关联。</span><span class="sxs-lookup"><span data-stu-id="58440-112">The item must be associated with a storage dimension group that has warehouse management process enabled.</span></span>
- <span data-ttu-id="58440-113">使用的仓库必须启用可供仓库管理流程使用，并且用于接收的库位必须受牌照控制。</span><span class="sxs-lookup"><span data-stu-id="58440-113">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span>

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a><span data-ttu-id="58440-114">创建使用仓库管理的物料到达日记帐标题</span><span class="sxs-lookup"><span data-stu-id="58440-114">Create an item arrival journal header that uses warehouse management</span></span>

<span data-ttu-id="58440-115">以下场景显示了如何创建使用仓库管理的物料到达日记帐标题：</span><span class="sxs-lookup"><span data-stu-id="58440-115">The following scenario shows how to create an item arrival journal header that uses warehouse management:</span></span>

1. <span data-ttu-id="58440-116">确保您的系统包含满足上一部分中概述的要求的已确认采购订单。</span><span class="sxs-lookup"><span data-stu-id="58440-116">Make sure your system contains a confirmed purchase order that fulfils the requirements outlined in the previous section.</span></span> <span data-ttu-id="58440-117">此场景使用公司 *USMF*、供应商帐户 *1001*、仓库 *51* 的采购订单，其中包含物料编号 *M9200* 的 *10 PL*（10 个托盘）的订单行。</span><span class="sxs-lookup"><span data-stu-id="58440-117">This scenario uses a purchase order for company *USMF*, vendor account *1001*, warehouse *51*, with an order line for *10 PL* (10 pallets) of item number *M9200*.</span></span>
1. <span data-ttu-id="58440-118">记下将使用的采购订单编号。</span><span class="sxs-lookup"><span data-stu-id="58440-118">Make a note of the purchase order number that you will use.</span></span>
1. <span data-ttu-id="58440-119">转到 **库存管理 \> 日记帐条目 \> 物料到达 \> 物料到达**。</span><span class="sxs-lookup"><span data-stu-id="58440-119">Go to **Inventory management \> Journal entries \> Item arrival \> Item arrival**.</span></span>
1. <span data-ttu-id="58440-120">在操作窗格上选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="58440-120">Select **New** on the Action Pane.</span></span>
1. <span data-ttu-id="58440-121">**创建仓库管理日记帐** 对话框将打开。</span><span class="sxs-lookup"><span data-stu-id="58440-121">The **Create warehouse management journal** dialog box opens.</span></span> <span data-ttu-id="58440-122">在 **名称** 字段中选择日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="58440-122">Select a journal name in the **Name** field.</span></span>
    - <span data-ttu-id="58440-123">如果您使用 *USMF* 示例数据，选择 *WHS*。</span><span class="sxs-lookup"><span data-stu-id="58440-123">If you are using *USMF* sample data, select *WHS*.</span></span>
    - <span data-ttu-id="58440-124">如果您使用自己的数据，则选择的日记帐必须将 **检查领料库位** 设置为 *否* 并将 **检验管理** 设置为 *否*。</span><span class="sxs-lookup"><span data-stu-id="58440-124">If you're using your own data, the journal you choose must have **Check picking location** set to *No* and **Quarantine management** set to *No*.</span></span>
1. <span data-ttu-id="58440-125">将 **引用** 设置为 *采购订单*。</span><span class="sxs-lookup"><span data-stu-id="58440-125">Set **Reference** to *Purchase order*.</span></span>
1. <span data-ttu-id="58440-126">将 **帐户编号** 设置为 *1001*。</span><span class="sxs-lookup"><span data-stu-id="58440-126">Set **Account number** to *1001*.</span></span>
1. <span data-ttu-id="58440-127">将 **编号** 设置为您为此练习标识的采购订单的编号。</span><span class="sxs-lookup"><span data-stu-id="58440-127">Set **Number** to the number of the purchase order that you identified for this exercise.</span></span>

    <span data-ttu-id="58440-128">![物料到达日记帐](../media/item-arrival-journal-header.png "物料到达日记帐")</span><span class="sxs-lookup"><span data-stu-id="58440-128">![Item arrival journal](../media/item-arrival-journal-header.png "Item arrival journal")</span></span>

1. <span data-ttu-id="58440-129">选择 **确定** 以创建日记帐标题。</span><span class="sxs-lookup"><span data-stu-id="58440-129">Select the **OK** to create the journal header.</span></span>
1. <span data-ttu-id="58440-130">在 **日记帐行** 部分中，选择 **添加行** 并输入以下数据：</span><span class="sxs-lookup"><span data-stu-id="58440-130">In the **Journal lines** section, select **Add line** and enter the following data:</span></span>
    - <span data-ttu-id="58440-131">**物料编号** – 设置为 *M9200*。</span><span class="sxs-lookup"><span data-stu-id="58440-131">**Item number** – Set to *M9200*.</span></span> <span data-ttu-id="58440-132">将基于 10 个托盘（1000 个）的库存交易记录数据设置 **场地**、**仓库** 和 **数量**。</span><span class="sxs-lookup"><span data-stu-id="58440-132">The **Site**, **Warehouse**, and **Quantity** will get set based on the inventory transaction data for the 10 pallets (1000 ea.).</span></span>
    - <span data-ttu-id="58440-133">**库位** – 设置为 *001*。</span><span class="sxs-lookup"><span data-stu-id="58440-133">**Location** – Set to  *001*.</span></span> <span data-ttu-id="58440-134">此特定库位不跟踪牌照。</span><span class="sxs-lookup"><span data-stu-id="58440-134">This specific location does not track license plates.</span></span>

    <span data-ttu-id="58440-135">![物料到达日记帐行](../media/item-arrival-journal-line.png "物料到达日记帐行")</span><span class="sxs-lookup"><span data-stu-id="58440-135">![Item arrival journal line](../media/item-arrival-journal-line.png "Item arrival journal line")</span></span>

    > [!NOTE]
    > <span data-ttu-id="58440-136">**日期** 字段确定此现有数量的物料将记入库存的日期。</span><span class="sxs-lookup"><span data-stu-id="58440-136">The **Date** field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    >
    > <span data-ttu-id="58440-137">如果可从提供的信息个别识别，系统将会自动填充 **批次 ID**。</span><span class="sxs-lookup"><span data-stu-id="58440-137">The **Lot ID** will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="58440-138">否则将必须手动输入。</span><span class="sxs-lookup"><span data-stu-id="58440-138">Otherwise you will have to enter this manually.</span></span> <span data-ttu-id="58440-139">这是必填字段，用于将此登记链接到特定原始单据行。</span><span class="sxs-lookup"><span data-stu-id="58440-139">This is a required field, which links this registration to a specific source document line.</span></span>  

1. <span data-ttu-id="58440-140">在操作窗格上选择 **验证**。</span><span class="sxs-lookup"><span data-stu-id="58440-140">Select **Validate** on the Action Pane.</span></span> <span data-ttu-id="58440-141">这会检查准备好供过帐的日记帐。</span><span class="sxs-lookup"><span data-stu-id="58440-141">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="58440-142">如果验证失败，需要修复错误才能过帐日记帐。</span><span class="sxs-lookup"><span data-stu-id="58440-142">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
1. <span data-ttu-id="58440-143">**检查日记帐** 对话框将打开。</span><span class="sxs-lookup"><span data-stu-id="58440-143">The **Check journal** dialog box opens.</span></span> <span data-ttu-id="58440-144">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="58440-144">Select **OK**.</span></span>
1. <span data-ttu-id="58440-145">查看消息栏。</span><span class="sxs-lookup"><span data-stu-id="58440-145">Review the message bar.</span></span> <span data-ttu-id="58440-146">应该有一条消息表示操作已完成。</span><span class="sxs-lookup"><span data-stu-id="58440-146">There should be a message denoting that the operation was completed.</span></span>  
1. <span data-ttu-id="58440-147">在操作窗格上选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="58440-147">Select **Post** on the Action Pane.</span></span>
1. <span data-ttu-id="58440-148">**过帐日记帐** 对话框将打开。</span><span class="sxs-lookup"><span data-stu-id="58440-148">The **Post journal** dialog box opens.</span></span> <span data-ttu-id="58440-149">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="58440-149">Select **OK**.</span></span>
1. <span data-ttu-id="58440-150">查看消息栏。</span><span class="sxs-lookup"><span data-stu-id="58440-150">Review the message bar.</span></span> <span data-ttu-id="58440-151">应该有消息表示操作完成。</span><span class="sxs-lookup"><span data-stu-id="58440-151">There should be messages denoting that the operation completed.</span></span>
1. <span data-ttu-id="58440-152">在操作窗格上选择 **功能 > 产品收货** 以更新订单行并过帐产品收货。</span><span class="sxs-lookup"><span data-stu-id="58440-152">Select **Functions > Product receipt** on the Action Pane to update the purchase order line and post a product receipt.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
