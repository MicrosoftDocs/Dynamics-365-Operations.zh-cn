--- 
title: "审核特定采购类别的供应商"
description: "创建采购申请时，可能需要选择核准供应商或首选供应商，具体取决于制订的采购政策。"
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3ee04497653b21600cd42fa9c90e7876e613acee
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="6e6df-103">审核特定采购类别的供应商</span><span class="sxs-lookup"><span data-stu-id="6e6df-103">Approve vendors for specific procurement categories</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e6df-104">创建采购申请时，可能需要选择核准供应商或首选供应商，具体取决于制订的采购政策。</span><span class="sxs-lookup"><span data-stu-id="6e6df-104">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="6e6df-105">此过程演示如何指定供应商是特定采购类别的核准供应商或首选供应商。</span><span class="sxs-lookup"><span data-stu-id="6e6df-105">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="6e6df-106">此任务通常由采购专业人员完成。</span><span class="sxs-lookup"><span data-stu-id="6e6df-106">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="6e6df-107">您可以在演示数据公司 USMF 中使用此过程。</span><span class="sxs-lookup"><span data-stu-id="6e6df-107">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="6e6df-108">转到“采购”>“供应商”>“所有供应商”。</span><span class="sxs-lookup"><span data-stu-id="6e6df-108">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="6e6df-109">选择要设置为类别的核准供应商或首选供应商的供应商。</span><span class="sxs-lookup"><span data-stu-id="6e6df-109">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="6e6df-110">在操作窗格上，单击“常规”。</span><span class="sxs-lookup"><span data-stu-id="6e6df-110">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="6e6df-111">单击“类别”。</span><span class="sxs-lookup"><span data-stu-id="6e6df-111">Click Categories.</span></span>
5. <span data-ttu-id="6e6df-112">单击“添加类别”。</span><span class="sxs-lookup"><span data-stu-id="6e6df-112">Click Add category.</span></span>
6. <span data-ttu-id="6e6df-113">在“类别”字段中，选择“办公和桌面附件(办公和桌面附件)”。</span><span class="sxs-lookup"><span data-stu-id="6e6df-113">In the Category field, select OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES).</span></span>
7. <span data-ttu-id="6e6df-114">在“供应商类别状态”字段中，选择“首选”。</span><span class="sxs-lookup"><span data-stu-id="6e6df-114">In the Vendor category status field, select 'Preferred'.</span></span>
    * <span data-ttu-id="6e6df-115">可以为一个类别指定多家首选供应商。</span><span class="sxs-lookup"><span data-stu-id="6e6df-115">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="6e6df-116">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6e6df-116">Click Save.</span></span>
9. <span data-ttu-id="6e6df-117">转到采购>采购目录。 </span><span class="sxs-lookup"><span data-stu-id="6e6df-117">Go to Procurement and sourcing > Procurement categories.</span></span>
10. <span data-ttu-id="6e6df-118">在树中，选择“企业采购类别\办公和桌面附件“。</span><span class="sxs-lookup"><span data-stu-id="6e6df-118">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES'.</span></span>
11. <span data-ttu-id="6e6df-119">展开“供应商”部分。</span><span class="sxs-lookup"><span data-stu-id="6e6df-119">Expand the Vendors section.</span></span>
    * <span data-ttu-id="6e6df-120">检查所选供应商是否显示为办公室和桌面附件类别的首选供应商。</span><span class="sxs-lookup"><span data-stu-id="6e6df-120">Check if the vendor that you selected  appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="6e6df-121">如果您要将此过程作为任务指南运行，可能必须单击“解锁”按钮才能向下滚动到供应商列表。</span><span class="sxs-lookup"><span data-stu-id="6e6df-121">If you’re running this procedure as a task guide, you may have to click the Unlock button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="6e6df-122">还可以在此页中添加首选供应商和核准供应商。</span><span class="sxs-lookup"><span data-stu-id="6e6df-122">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="6e6df-123">在树中，展开“办公和桌面附件”。</span><span class="sxs-lookup"><span data-stu-id="6e6df-123">In the tree, expand 'OFFICE AND DESK ACCESSORIES'.</span></span>
13. <span data-ttu-id="6e6df-124">在树中，选择“剪刀”。</span><span class="sxs-lookup"><span data-stu-id="6e6df-124">In the tree, select 'Scissors'.</span></span>
14. <span data-ttu-id="6e6df-125">在“从父类别继承供应商:”字段中选择“否”。</span><span class="sxs-lookup"><span data-stu-id="6e6df-125">Select No in the Inherit vendors from parent category: field.</span></span>
15. <span data-ttu-id="6e6df-126">在“从父类别继承供应商:”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="6e6df-126">Select Yes in the Inherit vendors from parent category: field.</span></span>


