--- 
title: "对货运进行手动对帐"
description: "此过程显示如何手动对帐货运。"
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 15148725664d839694ede8419213d881c7be83dd
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="d1f58-103">对货运进行手动对帐</span><span class="sxs-lookup"><span data-stu-id="d1f58-103">Reconcile freight manually</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d1f58-104">此过程显示如何手动对帐货运。</span><span class="sxs-lookup"><span data-stu-id="d1f58-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="d1f58-105">这通常由运输协调员完成。</span><span class="sxs-lookup"><span data-stu-id="d1f58-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="d1f58-106">您可以在 USMF 演示数据公司中使用此过程。</span><span class="sxs-lookup"><span data-stu-id="d1f58-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="d1f58-107">选择要对帐的负荷</span><span class="sxs-lookup"><span data-stu-id="d1f58-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="d1f58-108">转到“运输管理”>“计划”>“装载计划工作台”。</span><span class="sxs-lookup"><span data-stu-id="d1f58-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="d1f58-109">清除“隐藏已装运和已接收”复选框。</span><span class="sxs-lookup"><span data-stu-id="d1f58-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="d1f58-110">在列表中，选择负荷 ID 为 00006 的负荷。</span><span class="sxs-lookup"><span data-stu-id="d1f58-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="d1f58-111">创建承运人发票</span><span class="sxs-lookup"><span data-stu-id="d1f58-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="d1f58-112">如果手动对帐货运，并且不自动接收承运人发票，可以基于货运帐单创建发票。</span><span class="sxs-lookup"><span data-stu-id="d1f58-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="d1f58-113">单击“相关信息”。</span><span class="sxs-lookup"><span data-stu-id="d1f58-113">Click Related information.</span></span>
2. <span data-ttu-id="d1f58-114">单击“货运帐单明细”。</span><span class="sxs-lookup"><span data-stu-id="d1f58-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="d1f58-115">单击“生成货运帐单发票”。</span><span class="sxs-lookup"><span data-stu-id="d1f58-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="d1f58-116">在“发票”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d1f58-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="d1f58-117">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d1f58-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="d1f58-118">对发票进行对帐</span><span class="sxs-lookup"><span data-stu-id="d1f58-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="d1f58-119">对帐承运人发票和货运帐单时，逐行执行。</span><span class="sxs-lookup"><span data-stu-id="d1f58-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="d1f58-120">单击“匹配货运帐单和发票”。</span><span class="sxs-lookup"><span data-stu-id="d1f58-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="d1f58-121">展开“发票详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="d1f58-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="d1f58-122">展开“已取消匹配的货运帐单明细”部分。</span><span class="sxs-lookup"><span data-stu-id="d1f58-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="d1f58-123">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="d1f58-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="d1f58-124">单击“匹配”。</span><span class="sxs-lookup"><span data-stu-id="d1f58-124">Click Match.</span></span>
6. <span data-ttu-id="d1f58-125">展开“匹配的货运帐单明细”部分。</span><span class="sxs-lookup"><span data-stu-id="d1f58-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="d1f58-126">提交发票以供审核</span><span class="sxs-lookup"><span data-stu-id="d1f58-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="d1f58-127">单击“提交以供审核”。</span><span class="sxs-lookup"><span data-stu-id="d1f58-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="d1f58-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d1f58-128">Close the page.</span></span>
3. <span data-ttu-id="d1f58-129">清除“隐藏已审核项”复选框。</span><span class="sxs-lookup"><span data-stu-id="d1f58-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="d1f58-130">单击“供应商发票日记帐”。</span><span class="sxs-lookup"><span data-stu-id="d1f58-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="d1f58-131">单击以访问“参考日记帐号”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="d1f58-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="d1f58-132">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="d1f58-132">Click Lines.</span></span>

