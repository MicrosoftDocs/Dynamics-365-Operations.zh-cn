---
title: 创建按预算管理的采购订单
description: 使用此过程可以创建为可用预算检查的采购订单。
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa16955e0ea407555c7b52b0af37c5891be9bdbb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214274"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="e3cb1-103">创建按预算管理的采购订单</span><span class="sxs-lookup"><span data-stu-id="e3cb1-103">Create a purchase order governed by budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3cb1-104">使用此过程可以创建为可用预算检查的采购订单。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="e3cb1-105">此录制使用 USMF 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="e3cb1-106">检查预算控制配置</span><span class="sxs-lookup"><span data-stu-id="e3cb1-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="e3cb1-107">转至“预算”>“设置”>“预算控制”>“预算控制配置”。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="e3cb1-108">单击“可用的预算资金”选项卡。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="e3cb1-109">单击“单据和日记帐”选项卡。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="e3cb1-110">单击“定义预算控制规则”选项卡。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="e3cb1-111">单击“定义预算组”选项卡。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="e3cb1-112">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="e3cb1-113">创建采购订单头</span><span class="sxs-lookup"><span data-stu-id="e3cb1-113">Create the purchase order header</span></span>
1. <span data-ttu-id="e3cb1-114">转到“采购”>“采购订单”>“所有采购订单”。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="e3cb1-115">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-115">Click New.</span></span>
3. <span data-ttu-id="e3cb1-116">在“供应商帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="e3cb1-117">展开“常规”部分。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-117">Expand the General section.</span></span>
5. <span data-ttu-id="e3cb1-118">在“会计日期”字段中，将日期设置为“2016-01-01”。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="e3cb1-119">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="e3cb1-120">添加采购订单行</span><span class="sxs-lookup"><span data-stu-id="e3cb1-120">Add a purchase order line</span></span>
1. <span data-ttu-id="e3cb1-121">在“采购类别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="e3cb1-122">将“数量”设置为“2”。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="e3cb1-123">在“单位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="e3cb1-124">将“单价”设置为“10000”。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="e3cb1-125">单击“财务”。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-125">Click Financials.</span></span>
6. <span data-ttu-id="e3cb1-126">单击“分配金额”。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="e3cb1-127">在“会计科目”字段中，指定值“601300-001-023--”。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="e3cb1-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="e3cb1-129">执行预算检查</span><span class="sxs-lookup"><span data-stu-id="e3cb1-129">Perform budget checking</span></span>
1. <span data-ttu-id="e3cb1-130">单击“财务”。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-130">Click Financials.</span></span>
2. <span data-ttu-id="e3cb1-131">单击“执行预算检查”。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="e3cb1-132">单击“财务”。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-132">Click Financials.</span></span>
4. <span data-ttu-id="e3cb1-133">单击“预算检查错误或警告”。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="e3cb1-134">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="e3cb1-134">Click Close.</span></span>

