--- 
title: "检查货物质量"
description: "此过程显示如何处理质检订单。"
author: perlynne
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: c2313ba26eac8abf6e603f0230f06103802536c4
ms.contentlocale: zh-cn
ms.lasthandoff: 09/11/2018

---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="33dc5-103">检查货物质量</span><span class="sxs-lookup"><span data-stu-id="33dc5-103">Inspect the quality of goods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="33dc5-104">此过程显示如何处理质检订单。</span><span class="sxs-lookup"><span data-stu-id="33dc5-104">This procedure shows you how to process a quality order.</span></span> <span data-ttu-id="33dc5-105">您可以使用 USMF 公司演示数据运行此指南。</span><span class="sxs-lookup"><span data-stu-id="33dc5-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="33dc5-106">在开始此示例过程前，需要确认采购订单为“000016”，并且将产品收据过帐。</span><span class="sxs-lookup"><span data-stu-id="33dc5-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="33dc5-107">这将自动创建质检订单。</span><span class="sxs-lookup"><span data-stu-id="33dc5-107">This will automatically create a quality order.</span></span> <span data-ttu-id="33dc5-108">质量检查通常由质检员执行。</span><span class="sxs-lookup"><span data-stu-id="33dc5-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="33dc5-109">选择质检订单。</span><span class="sxs-lookup"><span data-stu-id="33dc5-109">Select a quality order</span></span>
1. <span data-ttu-id="33dc5-110">转到“库存管理”>“定期任务”>“质量管理”>“质检订单”。</span><span class="sxs-lookup"><span data-stu-id="33dc5-110">Go to Inventory management > Periodic tasks > Quality management > Quality orders.</span></span>
2. <span data-ttu-id="33dc5-111">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="33dc5-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="33dc5-112">在开始此过程前，选择已创建的质检订单。</span><span class="sxs-lookup"><span data-stu-id="33dc5-112">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="33dc5-113">记录测试结果</span><span class="sxs-lookup"><span data-stu-id="33dc5-113">Record test results</span></span>
1. <span data-ttu-id="33dc5-114">单击“结果”。</span><span class="sxs-lookup"><span data-stu-id="33dc5-114">Click Results.</span></span>
2. <span data-ttu-id="33dc5-115">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="33dc5-115">Click Edit.</span></span>
3. <span data-ttu-id="33dc5-116">在“结果数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="33dc5-116">In the Result quantity field, enter a number.</span></span>
4. <span data-ttu-id="33dc5-117">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="33dc5-117">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="33dc5-118">在“结果”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="33dc5-118">In the Outcome field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="33dc5-119">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="33dc5-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="33dc5-120">在此示例中，结果将基于预定义的结果。</span><span class="sxs-lookup"><span data-stu-id="33dc5-120">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="33dc5-121">通常您可以记录更具体的测试结果，例如大小或其他维度。</span><span class="sxs-lookup"><span data-stu-id="33dc5-121">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
7. <span data-ttu-id="33dc5-122">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="33dc5-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="33dc5-123">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="33dc5-123">Click Save.</span></span>
9. <span data-ttu-id="33dc5-124">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="33dc5-124">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="33dc5-125">验证质检订单</span><span class="sxs-lookup"><span data-stu-id="33dc5-125">Validate the quality order</span></span>
1. <span data-ttu-id="33dc5-126">单击“验证”。</span><span class="sxs-lookup"><span data-stu-id="33dc5-126">Click Validate.</span></span>
2. <span data-ttu-id="33dc5-127">在“验证人员”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="33dc5-127">In the Validated by field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="33dc5-128">选择执行检查的用户。</span><span class="sxs-lookup"><span data-stu-id="33dc5-128">Select the user performing the inspection.</span></span>  
3. <span data-ttu-id="33dc5-129">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="33dc5-129">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="33dc5-130">单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="33dc5-130">Click Select.</span></span>
5. <span data-ttu-id="33dc5-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="33dc5-131">Click OK.</span></span>
6. <span data-ttu-id="33dc5-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="33dc5-132">Close the page.</span></span>


