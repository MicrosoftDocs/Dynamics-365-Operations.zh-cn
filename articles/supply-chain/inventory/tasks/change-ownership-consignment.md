---
title: "根据生产需求更改托运库存的所有权"
description: "此过程显示在生产需要库存时，如何将托运库存的所有者从供应商更改为法人。"
author: perlynne
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e3058987dcd511c59a9eae1b79ef5d1b6d4b3d68
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="9aaf6-103">根据生产需求更改托运库存的所有权</span><span class="sxs-lookup"><span data-stu-id="9aaf6-103">Change the ownership of consignment inventory based on production demand</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9aaf6-104">此过程显示在生产需要库存时，如何将托运库存的所有者从供应商更改为法人。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="9aaf6-105">所有权的此项更改通过创建并过帐库存所有权更改日记帐完成。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="9aaf6-106">所有权更改日记帐行可以手动创建，也可以根据现有生产需要按照此记录中的显示创建。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="9aaf6-107">通常由车间主管执行此任务。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="9aaf6-108">您可以在 USMF 演示数据公司，也可在您自己的数据中运行该过程。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="9aaf6-109">如果您在使用自己的数据，请确保已满足以下先决条件：为库存所有权更改设置的库存日记帐名称、物理记录且由供应商拥有的现成物料，以及材料的一个或多个生产订单行。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="9aaf6-110">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="9aaf6-111">创建库存所有权日记帐</span><span class="sxs-lookup"><span data-stu-id="9aaf6-111">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="9aaf6-112">转到“库存管理”>“日记帐条目”>“物料”>“库存所有权更改”。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-112">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="9aaf6-113">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-113">Click New.</span></span>
    * <span data-ttu-id="9aaf6-114">库存所有权更改日记帐用于更改供应商到当前法人的托运库存的所有者。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-114">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="9aaf6-115">所有权的此项更改通过发放供应商拥有的现有库存，然后在当前法人处接收该库存完成。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-115">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="9aaf6-116">在“名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-116">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="9aaf6-117">可以选择日记帐类型为“所有权更改”的库存日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-117">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="9aaf6-118">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-118">Click OK.</span></span>
5. <span data-ttu-id="9aaf6-119">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-119">Click Functions.</span></span>
6. <span data-ttu-id="9aaf6-120">单击“通过生产订单创建日记帐行”。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-120">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="9aaf6-121">可以通过查询需要消耗原材料的所有生产行，启动更改所有权流程。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-121">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="9aaf6-122">在“要包含的库存发货状态”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-122">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="9aaf6-123">此选项用于按库存交易的发货状态筛选。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-123">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="9aaf6-124">例如，您可以为“已拣货”和“物理保留”状态创建日记帐行。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-124">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="9aaf6-125">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-125">Expand the Records to include section.</span></span>
    * <span data-ttu-id="9aaf6-126">此部分用于应用更多筛选。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-126">This section lets you apply additional filtering.</span></span> <span data-ttu-id="9aaf6-127">例如，可以选择特定原材料日期。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-127">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="9aaf6-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-128">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="9aaf6-129">过帐库存所有权更改日记帐</span><span class="sxs-lookup"><span data-stu-id="9aaf6-129">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="9aaf6-130">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-130">Click Post.</span></span>
    * <span data-ttu-id="9aaf6-131">在过帐日记帐时，将使用“所有权更改”引用发放供应商拥有的库存。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-131">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="9aaf6-132">然后使用通过采购订单物料收据更新的库存交易，将库存作为现有量接收。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-132">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="9aaf6-133">请注意，将仅创建与过帐的日记帐有关的交易。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-133">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="9aaf6-134">不创建任何预期库存交易。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-134">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="9aaf6-135">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-135">Click OK.</span></span>
3. <span data-ttu-id="9aaf6-136">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9aaf6-136">Close the page.</span></span>

