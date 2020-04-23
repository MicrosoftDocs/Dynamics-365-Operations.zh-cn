---
title: 根据生产需求更改托运库存的所有权
description: 此过程显示在生产需要库存时，如何将托运库存的所有者从供应商更改为法人。
author: perlynne
manager: tfehr
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c50affa05b8df53d31660854f4d1ead6aeff820
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204232"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="c4370-103">根据生产需求更改托运库存的所有权</span><span class="sxs-lookup"><span data-stu-id="c4370-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c4370-104">此过程显示在生产需要库存时，如何将托运库存的所有者从供应商更改为法人。</span><span class="sxs-lookup"><span data-stu-id="c4370-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="c4370-105">所有权的此项更改通过创建并过帐库存所有权更改日记帐完成。</span><span class="sxs-lookup"><span data-stu-id="c4370-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="c4370-106">所有权更改日记帐行可以手动创建，也可以根据现有生产需要按照此记录中的显示创建。</span><span class="sxs-lookup"><span data-stu-id="c4370-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="c4370-107">通常由车间主管执行此任务。</span><span class="sxs-lookup"><span data-stu-id="c4370-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="c4370-108">您可以在 USMF 演示数据公司，也可在您自己的数据中运行该过程。</span><span class="sxs-lookup"><span data-stu-id="c4370-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="c4370-109">如果您在使用自己的数据，请确保已满足以下先决条件：为库存所有权更改设置的库存日记帐名称、物理记录且由供应商拥有的现成物料，以及材料的一个或多个生产订单行。</span><span class="sxs-lookup"><span data-stu-id="c4370-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="c4370-110">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="c4370-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

> [!NOTE]
> <span data-ttu-id="c4370-111">默认不支持出站托运流程，也不支持所有权日记帐自动处理。</span><span class="sxs-lookup"><span data-stu-id="c4370-111">Outbound consignment processes are not supported out-of-the-box and automatic ownership journal processing is not supported.</span></span>

## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="c4370-112">创建库存所有权日记帐</span><span class="sxs-lookup"><span data-stu-id="c4370-112">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="c4370-113">转到“库存管理”>“日记帐条目”>“物料”>“库存所有权更改”。</span><span class="sxs-lookup"><span data-stu-id="c4370-113">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="c4370-114">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="c4370-114">Click New.</span></span>
    * <span data-ttu-id="c4370-115">库存所有权更改日记帐用于更改供应商到当前法人的托运库存的所有者。</span><span class="sxs-lookup"><span data-stu-id="c4370-115">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="c4370-116">所有权的此项更改通过发放供应商拥有的现有库存，然后在当前法人处接收该库存完成。</span><span class="sxs-lookup"><span data-stu-id="c4370-116">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="c4370-117">在“名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c4370-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="c4370-118">可以选择日记帐类型为“所有权更改”的库存日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="c4370-118">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="c4370-119">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="c4370-119">Click OK.</span></span>
5. <span data-ttu-id="c4370-120">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="c4370-120">Click Functions.</span></span>
6. <span data-ttu-id="c4370-121">单击“通过生产订单创建日记帐行”。</span><span class="sxs-lookup"><span data-stu-id="c4370-121">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="c4370-122">可以通过查询需要消耗原材料的所有生产行，启动更改所有权流程。</span><span class="sxs-lookup"><span data-stu-id="c4370-122">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="c4370-123">在“要包含的库存发货状态”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="c4370-123">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="c4370-124">此选项用于按库存交易的发货状态筛选。</span><span class="sxs-lookup"><span data-stu-id="c4370-124">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="c4370-125">例如，您可以为“已拣货”和“物理保留”状态创建日记帐行。</span><span class="sxs-lookup"><span data-stu-id="c4370-125">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="c4370-126">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="c4370-126">Expand the Records to include section.</span></span>
    * <span data-ttu-id="c4370-127">此部分用于应用更多筛选。</span><span class="sxs-lookup"><span data-stu-id="c4370-127">This section lets you apply additional filtering.</span></span> <span data-ttu-id="c4370-128">例如，可以选择特定原材料日期。</span><span class="sxs-lookup"><span data-stu-id="c4370-128">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="c4370-129">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="c4370-129">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="c4370-130">过帐库存所有权更改日记帐</span><span class="sxs-lookup"><span data-stu-id="c4370-130">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="c4370-131">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="c4370-131">Click Post.</span></span>
    * <span data-ttu-id="c4370-132">在过帐日记帐时，将使用“所有权更改”引用发放供应商拥有的库存。</span><span class="sxs-lookup"><span data-stu-id="c4370-132">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="c4370-133">然后使用通过采购订单物料收据更新的库存交易，将库存作为现有量接收。</span><span class="sxs-lookup"><span data-stu-id="c4370-133">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="c4370-134">请注意，将仅创建与过帐的日记帐有关的交易。</span><span class="sxs-lookup"><span data-stu-id="c4370-134">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="c4370-135">不创建任何预期库存交易。</span><span class="sxs-lookup"><span data-stu-id="c4370-135">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="c4370-136">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="c4370-136">Click OK.</span></span>
3. <span data-ttu-id="c4370-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c4370-137">Close the page.</span></span>

