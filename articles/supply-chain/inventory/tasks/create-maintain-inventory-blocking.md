---
title: 创建和维护库存锁定
description: 此过程显示如何通过使用库存锁定防止实际现有库存由其他出货原始凭证预留。
author: perlynne
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2485eaf31226b11106895074ae0ad95e561777b
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916591"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="b7a34-103">创建和维护库存锁定</span><span class="sxs-lookup"><span data-stu-id="b7a34-103">Create and maintain an inventory blocking</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b7a34-104">此过程显示如何通过使用库存锁定防止实际现有库存由其他出货原始凭证预留。</span><span class="sxs-lookup"><span data-stu-id="b7a34-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="b7a34-105">您可以使用所示的示例值运行 USMF 公司演示数据的过程。</span><span class="sxs-lookup"><span data-stu-id="b7a34-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="b7a34-106">在开始此过程前，需要有物料和可用的实际现有库存。</span><span class="sxs-lookup"><span data-stu-id="b7a34-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="b7a34-107">创建库存锁定</span><span class="sxs-lookup"><span data-stu-id="b7a34-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="b7a34-108">在**导航窗格**中，转到**模块 > 库存管理 > 定期任务 > 库存锁定**。</span><span class="sxs-lookup"><span data-stu-id="b7a34-108">In the **Navigation pane**, go to **Modules > Inventory management > Periodic tasks > Inventory blocking**.</span></span>
2. <span data-ttu-id="b7a34-109">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="b7a34-109">Click **New**.</span></span>
3. <span data-ttu-id="b7a34-110">在**物料编号**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b7a34-110">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b7a34-111">在列表中，选择您想选的物料。</span><span class="sxs-lookup"><span data-stu-id="b7a34-111">In the list, select the item you want to choose.</span></span> <span data-ttu-id="b7a34-112">选择物料编号以及您想要锁定的实际现有库存。</span><span class="sxs-lookup"><span data-stu-id="b7a34-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="b7a34-113">如果您使用 USMF，您可以选择物料 M9201。</span><span class="sxs-lookup"><span data-stu-id="b7a34-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="b7a34-114">在**数量**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="b7a34-114">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="b7a34-115">如果您使用物料 M9201，需要选择少于 200。</span><span class="sxs-lookup"><span data-stu-id="b7a34-115">If you’re using item M9201, you need to select less than 200.</span></span>
6. <span data-ttu-id="b7a34-116">展开**库存维度**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="b7a34-116">Expand the **Inventory dimensions** fastTab.</span></span>
7. <span data-ttu-id="b7a34-117">在**仓库**字段，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b7a34-117">In the **Warehouse** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="b7a34-118">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b7a34-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="b7a34-119">如果您使用物料 M9201，您可以选择仓库 51。</span><span class="sxs-lookup"><span data-stu-id="b7a34-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="b7a34-120">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="b7a34-120">Click **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="b7a34-121">更新库存锁定的条件</span><span class="sxs-lookup"><span data-stu-id="b7a34-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="b7a34-122">在**常规**快速选项卡的**数量**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="b7a34-122">In the **General** fastTab, in the **Quantity** field, enter a number.</span></span> <span data-ttu-id="b7a34-123">更新“库存数量”字段以反映锁定数量。</span><span class="sxs-lookup"><span data-stu-id="b7a34-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="b7a34-124">在**预期日期**字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="b7a34-124">In the **Expected date** field, enter a date.</span></span> <span data-ttu-id="b7a34-125">您可能希望通过分配预期日期，指定锁定的库存什么时候可供使用。</span><span class="sxs-lookup"><span data-stu-id="b7a34-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="b7a34-126">如果为库存锁定选择所需的收据选项，由于在您手动创建锁定时为默认显示，该日期将出现在预期事务中。</span><span class="sxs-lookup"><span data-stu-id="b7a34-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="b7a34-127">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="b7a34-127">Click **Save**.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="b7a34-128">取消库存锁定</span><span class="sxs-lookup"><span data-stu-id="b7a34-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="b7a34-129">在**操作窗格**上，单击**删除**。</span><span class="sxs-lookup"><span data-stu-id="b7a34-129">On the **Action pane**, click **Delete**.</span></span>
2. <span data-ttu-id="b7a34-130">单击**是**。</span><span class="sxs-lookup"><span data-stu-id="b7a34-130">Click **Yes**.</span></span>
3. <span data-ttu-id="b7a34-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b7a34-131">Close the page.</span></span>

