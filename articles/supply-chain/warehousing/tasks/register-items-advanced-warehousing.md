--- 
title: "使用物料到达日记帐登记启用了高级仓库的物料"
description: "此过程说明了在使用高级仓库管理流程时如何使用物料到达日记帐登记物料。"
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 751e73be385606bc706b2e14ea83c1b56c96402c
ms.contentlocale: zh-cn
ms.lasthandoff: 09/11/2018

---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="3823c-103">使用物料到达日记帐登记启用了高级仓库的物料</span><span class="sxs-lookup"><span data-stu-id="3823c-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3823c-104">此过程说明了在使用高级仓库管理流程时如何使用物料到达日记帐登记物料。</span><span class="sxs-lookup"><span data-stu-id="3823c-104">This procedure shows you how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="3823c-105">这将通常由一个收料员完成。</span><span class="sxs-lookup"><span data-stu-id="3823c-105">This would usually be done by a receiving clerk.</span></span> 

<span data-ttu-id="3823c-106">您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="3823c-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="3823c-107">在开始本指南前，您需要使用未结采购订单行以确认采购订单。</span><span class="sxs-lookup"><span data-stu-id="3823c-107">You need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="3823c-108">该行上的物料必须进行存储，并且不可使用产品变型，亦不能具有跟踪维度。</span><span class="sxs-lookup"><span data-stu-id="3823c-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="3823c-109">并且该物料需要与启用仓库维度组的仓库管理流程关联。</span><span class="sxs-lookup"><span data-stu-id="3823c-109">And the item needs to be associated with a warehouse management process enabled storage dimension group.</span></span> <span data-ttu-id="3823c-110">使用的仓库必须启用可供仓库管理流程使用，并且用于接收的库位必须受牌照控制。</span><span class="sxs-lookup"><span data-stu-id="3823c-110">The warehouse that’s used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span> <span data-ttu-id="3823c-111">如果您使用 USMF，您可以使用公司帐户 1001、仓库 51 和物料 M9200 来创建采购订单。</span><span class="sxs-lookup"><span data-stu-id="3823c-111">If you’re using USMF, you can use company account 1001, Warehouse 51, and item M9200 to create your PO.</span></span> 

<span data-ttu-id="3823c-112">记下创建的采购订单的编号，以及用于采购订单行的物料编号库位。</span><span class="sxs-lookup"><span data-stu-id="3823c-112">Make a note of the number of the purchase order that you create, and also note the item number and the site that you used for your purchase order line.</span></span>


## <a name="create-an-item-arrival-journal-header"></a><span data-ttu-id="3823c-113">创建一个物料到达日记帐标题</span><span class="sxs-lookup"><span data-stu-id="3823c-113">Create an item arrival journal header</span></span>
1. <span data-ttu-id="3823c-114">转到“物料到达”。</span><span class="sxs-lookup"><span data-stu-id="3823c-114">Go to Item arrival.</span></span>
2. <span data-ttu-id="3823c-115">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="3823c-115">Click New.</span></span>
3. <span data-ttu-id="3823c-116">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3823c-116">In the Name field, type a value.</span></span>
    * <span data-ttu-id="3823c-117">如果您正在使用 USMF，可以键入 WHS。</span><span class="sxs-lookup"><span data-stu-id="3823c-117">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="3823c-118">如果您正在使用其他数据，您选择的日记帐名称必须具有以下属性：“检查领料库位”必须设置为“否”，以及“检验管理”必须设置为“否”。</span><span class="sxs-lookup"><span data-stu-id="3823c-118">If you’re using other data, the journal whose name you choose has to have the following properties: Check picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="3823c-119">在“编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="3823c-119">In the Number field, type a value.</span></span>
5. <span data-ttu-id="3823c-120">在“站点”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="3823c-120">In the Site field, type a value.</span></span>
    * <span data-ttu-id="3823c-121">选择您为采购订单行使用的站点。</span><span class="sxs-lookup"><span data-stu-id="3823c-121">Select the site that you used for your purchase order line.</span></span> <span data-ttu-id="3823c-122">这将用作默认值，将默认为日记帐中的所有行。</span><span class="sxs-lookup"><span data-stu-id="3823c-122">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="3823c-123">如果您在 USMF 中使用仓库 51，则选择站点 5。</span><span class="sxs-lookup"><span data-stu-id="3823c-123">If you used warehouse 51 in USMF, choose site 5.</span></span>  
6. <span data-ttu-id="3823c-124">在“仓库”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3823c-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="3823c-125">为所选站点选择有效的仓库。</span><span class="sxs-lookup"><span data-stu-id="3823c-125">Select a valid warehouse for the site that you’ve selected.</span></span> <span data-ttu-id="3823c-126">这将用作默认值，将默认为日记帐中的所有行。</span><span class="sxs-lookup"><span data-stu-id="3823c-126">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="3823c-127">如果您在 USMF 中使用示例值，则选择 51。</span><span class="sxs-lookup"><span data-stu-id="3823c-127">If you’re using the example values in USMF, select 51.</span></span>  
7. <span data-ttu-id="3823c-128">在“地点”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3823c-128">In the Location field, type a value.</span></span>
    * <span data-ttu-id="3823c-129">在所选仓库中选择一个有效库位。</span><span class="sxs-lookup"><span data-stu-id="3823c-129">Select a valid location in the warehouse that you’ve selected.</span></span> <span data-ttu-id="3823c-130">该库位必须与受牌照控制的库位资料有关。</span><span class="sxs-lookup"><span data-stu-id="3823c-130">The location has to be associated with a location profile, which is license plate controlled.</span></span> <span data-ttu-id="3823c-131">这将用作默认值，将默认为日记帐中的所有行。</span><span class="sxs-lookup"><span data-stu-id="3823c-131">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="3823c-132">如果您在 USMF 中使用示例值，则选择“散装 - 008”。</span><span class="sxs-lookup"><span data-stu-id="3823c-132">If you’re using the example values in USMF, select Bulk-008.</span></span>  
8. <span data-ttu-id="3823c-133">右键单击牌照字段的下拉箭头，然后选择“查看详细信息”。</span><span class="sxs-lookup"><span data-stu-id="3823c-133">Right-click on the drop-down arrow in the License plate field and then select View details.</span></span>
9. <span data-ttu-id="3823c-134">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="3823c-134">Click New.</span></span>
10. <span data-ttu-id="3823c-135">在“牌照”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3823c-135">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="3823c-136">记录数值。</span><span class="sxs-lookup"><span data-stu-id="3823c-136">Make a note of the value.</span></span>  
11. <span data-ttu-id="3823c-137">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="3823c-137">Click Save.</span></span>
12. <span data-ttu-id="3823c-138">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3823c-138">Close the page.</span></span>
13. <span data-ttu-id="3823c-139">在“牌照”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3823c-139">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="3823c-140">输入您刚创建牌照的值。</span><span class="sxs-lookup"><span data-stu-id="3823c-140">Enter the value of the license plate that you just created.</span></span> <span data-ttu-id="3823c-141">这将用作默认值，将默认为日记帐中的所有行。</span><span class="sxs-lookup"><span data-stu-id="3823c-141">This will serve as a default value, which will default to all lines in the journal.</span></span>  
14. <span data-ttu-id="3823c-142">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3823c-142">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="3823c-143">添加行</span><span class="sxs-lookup"><span data-stu-id="3823c-143">Add a line</span></span>
1. <span data-ttu-id="3823c-144">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="3823c-144">Click Add line.</span></span>
2. <span data-ttu-id="3823c-145">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="3823c-145">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="3823c-146">输入您在采购订单行使用的物料编号。</span><span class="sxs-lookup"><span data-stu-id="3823c-146">Enter the item number that you used on the purchase order line.</span></span>  
3. <span data-ttu-id="3823c-147">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="3823c-147">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="3823c-148">输入您想要登记的数量。</span><span class="sxs-lookup"><span data-stu-id="3823c-148">Enter the quantity that you want to register.</span></span>  
    * <span data-ttu-id="3823c-149">日期字段确定此现有数量的物料将记入库存的日期。</span><span class="sxs-lookup"><span data-stu-id="3823c-149">The Date field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    * <span data-ttu-id="3823c-150">如果可从提供的信息个别识别，系统将会自动填充批次 ID。</span><span class="sxs-lookup"><span data-stu-id="3823c-150">The lot ID will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="3823c-151">否则将必须手动添加。</span><span class="sxs-lookup"><span data-stu-id="3823c-151">Otherwise you will have to add this manually.</span></span> <span data-ttu-id="3823c-152">此为必填字段，其将此登记链接到特定原始凭证行。</span><span class="sxs-lookup"><span data-stu-id="3823c-152">This is a mandatory field, which links this registration to a specific source document line.</span></span>  

## <a name="complete-the-registration"></a><span data-ttu-id="3823c-153">完成登记</span><span class="sxs-lookup"><span data-stu-id="3823c-153">Complete the registration</span></span>
1. <span data-ttu-id="3823c-154">单击“验证”。</span><span class="sxs-lookup"><span data-stu-id="3823c-154">Click Validate.</span></span>
    * <span data-ttu-id="3823c-155">这会检查准备好供过帐的日记帐。</span><span class="sxs-lookup"><span data-stu-id="3823c-155">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="3823c-156">如果验证失败，需要修复错误才能过帐日记帐。</span><span class="sxs-lookup"><span data-stu-id="3823c-156">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
2. <span data-ttu-id="3823c-157">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3823c-157">Click OK.</span></span>
    * <span data-ttu-id="3823c-158">单击“确定”后，请检查消息。</span><span class="sxs-lookup"><span data-stu-id="3823c-158">After you clicked OK, check the message.</span></span> <span data-ttu-id="3823c-159">应该有条消息告知日记帐过帐成功。</span><span class="sxs-lookup"><span data-stu-id="3823c-159">There should be a message saying that the journal is OK.</span></span>  
3. <span data-ttu-id="3823c-160">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="3823c-160">Click Post.</span></span>
4. <span data-ttu-id="3823c-161">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3823c-161">Click OK.</span></span>
    * <span data-ttu-id="3823c-162">单击“确定”后，请检查消息栏。</span><span class="sxs-lookup"><span data-stu-id="3823c-162">After you have clicked OK, check the message bar.</span></span> <span data-ttu-id="3823c-163">应该有条消息告知操作成功。</span><span class="sxs-lookup"><span data-stu-id="3823c-163">There should be a message saying that the operation completed.</span></span>  
5. <span data-ttu-id="3823c-164">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3823c-164">Close the page.</span></span>


