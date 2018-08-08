---
title: "创建和维护库存锁定"
description: "此过程显示如何通过使用库存锁定防止实际现有库存由其他出货原始凭证预留。"
author: perlynne
manager: AnnBe
ms.date: 12/02/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 5c3e05439dec8395066c7cf00afa248571ea0abc
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---
# <a name="create-and-maintain-inventory-blocking"></a><span data-ttu-id="21f5c-103">创建和维护库存锁定</span><span class="sxs-lookup"><span data-stu-id="21f5c-103">Create and maintain inventory blocking</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="21f5c-104">此过程显示如何通过使用库存锁定防止实际现有库存由其他出货原始凭证预留。</span><span class="sxs-lookup"><span data-stu-id="21f5c-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="21f5c-105">您可以使用所示的示例值运行 USMF 公司演示数据的过程。</span><span class="sxs-lookup"><span data-stu-id="21f5c-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="21f5c-106">在开始此过程前，需要有物料和可用的实际现有库存。</span><span class="sxs-lookup"><span data-stu-id="21f5c-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="21f5c-107">创建库存锁定</span><span class="sxs-lookup"><span data-stu-id="21f5c-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="21f5c-108">转到“库存管理”>“定期任务”>“库存锁定”。</span><span class="sxs-lookup"><span data-stu-id="21f5c-108">Go to Inventory management > Periodic tasks > Inventory blocking.</span></span>
2. <span data-ttu-id="21f5c-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="21f5c-109">Click New.</span></span>
3. <span data-ttu-id="21f5c-110">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="21f5c-110">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="21f5c-111">在列表中，选择您想选的物料。</span><span class="sxs-lookup"><span data-stu-id="21f5c-111">In the list, select the item you want to choose.</span></span>
    * <span data-ttu-id="21f5c-112">选择物料编号以及您想要锁定的实际现有库存。</span><span class="sxs-lookup"><span data-stu-id="21f5c-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="21f5c-113">如果您使用 USMF，您可以选择物料 M9201。</span><span class="sxs-lookup"><span data-stu-id="21f5c-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="21f5c-114">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="21f5c-114">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="21f5c-115">如果您使用物料 M9201，需要选择少于 200。</span><span class="sxs-lookup"><span data-stu-id="21f5c-115">If you’re using item M9201, you need to select less than 200.</span></span>  
6. <span data-ttu-id="21f5c-116">切换“库存维度”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="21f5c-116">Toggle the expansion of the Inventory dimensions section.</span></span>
7. <span data-ttu-id="21f5c-117">在“仓库”字段，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="21f5c-117">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="21f5c-118">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="21f5c-118">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="21f5c-119">如果您使用物料 M9201，您可以选择仓库 51。</span><span class="sxs-lookup"><span data-stu-id="21f5c-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="21f5c-120">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="21f5c-120">Click Save.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="21f5c-121">更新库存锁定的条件</span><span class="sxs-lookup"><span data-stu-id="21f5c-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="21f5c-122">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="21f5c-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="21f5c-123">更新“库存数量”字段以反映锁定数量。</span><span class="sxs-lookup"><span data-stu-id="21f5c-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="21f5c-124">在“预期日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="21f5c-124">In the Expected date field, enter a date.</span></span>
    * <span data-ttu-id="21f5c-125">您可能希望通过分配预期日期，指定锁定的库存什么时候可供使用。</span><span class="sxs-lookup"><span data-stu-id="21f5c-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="21f5c-126">如果为库存锁定选择所需的收据选项，由于在您手动创建锁定时为默认显示，该日期将出现在预期事务中。</span><span class="sxs-lookup"><span data-stu-id="21f5c-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="21f5c-127">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="21f5c-127">Click Save.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="21f5c-128">取消库存锁定</span><span class="sxs-lookup"><span data-stu-id="21f5c-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="21f5c-129">单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="21f5c-129">Click Delete.</span></span>
2. <span data-ttu-id="21f5c-130">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="21f5c-130">Click Yes.</span></span>
3. <span data-ttu-id="21f5c-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="21f5c-131">Close the page.</span></span>

