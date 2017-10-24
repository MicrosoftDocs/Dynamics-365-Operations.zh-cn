--- 
title: "拆分固定资产"
description: "此任务指南将把一个资产帐簿的一定百分百拆分到新资产帐簿。"
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b4c1b39bcae1fa3830f3a217d1ad89e84cd72134
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="93b0d-103">拆分固定资产</span><span class="sxs-lookup"><span data-stu-id="93b0d-103">Split a fixed asset</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="93b0d-104">此任务指南将把一个资产帐簿的一定百分百拆分到新资产帐簿。</span><span class="sxs-lookup"><span data-stu-id="93b0d-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="93b0d-105">它使用会计角色和 USMF 演示数据。</span><span class="sxs-lookup"><span data-stu-id="93b0d-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="93b0d-106">创建新的固定资产</span><span class="sxs-lookup"><span data-stu-id="93b0d-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="93b0d-107">转到“固定资产”>“固定资产”>“固定资产”。</span><span class="sxs-lookup"><span data-stu-id="93b0d-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="93b0d-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="93b0d-108">Click New.</span></span>
3. <span data-ttu-id="93b0d-109">在“固定资产组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="93b0d-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="93b0d-110">请注意，固定资产编号将在稍后的拆分流程使用。</span><span class="sxs-lookup"><span data-stu-id="93b0d-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="93b0d-111">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="93b0d-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="93b0d-112">关闭窗体。</span><span class="sxs-lookup"><span data-stu-id="93b0d-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="93b0d-113">拆分固定资产</span><span class="sxs-lookup"><span data-stu-id="93b0d-113">Split a fixed asset</span></span>
1. <span data-ttu-id="93b0d-114">在列表中，查找并选择要拆分的固定资产。</span><span class="sxs-lookup"><span data-stu-id="93b0d-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="93b0d-115">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="93b0d-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="93b0d-116">单击“帐簿”。</span><span class="sxs-lookup"><span data-stu-id="93b0d-116">Click Books.</span></span>
    * <span data-ttu-id="93b0d-117">选择拆分到新资产的帐簿</span><span class="sxs-lookup"><span data-stu-id="93b0d-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="93b0d-118">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="93b0d-118">Click Functions.</span></span>
5. <span data-ttu-id="93b0d-119">单击“拆分固定资产”。</span><span class="sxs-lookup"><span data-stu-id="93b0d-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="93b0d-120">在“目标固定资产”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="93b0d-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="93b0d-121">在“目标帐簿”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="93b0d-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="93b0d-122">在“交易记录日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="93b0d-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="93b0d-123">在“百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="93b0d-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="93b0d-124">在“日记帐名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="93b0d-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="93b0d-125">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="93b0d-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="93b0d-126">过帐日记帐交易记录</span><span class="sxs-lookup"><span data-stu-id="93b0d-126">Post the journal transaction</span></span>
1. <span data-ttu-id="93b0d-127">转到固定资产>流水输入项>固定资产流水。</span><span class="sxs-lookup"><span data-stu-id="93b0d-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="93b0d-128">在列表中，选择在拆分流程创建的日记帐。</span><span class="sxs-lookup"><span data-stu-id="93b0d-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="93b0d-129">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="93b0d-129">Click Lines.</span></span>
    * <span data-ttu-id="93b0d-130">验证已创建的日记帐行。</span><span class="sxs-lookup"><span data-stu-id="93b0d-130">Verify the journal lines created.</span></span>  <span data-ttu-id="93b0d-131">创建原始资产的购置调整交易记录，以通过拆分流程指定的百分比减少价值。</span><span class="sxs-lookup"><span data-stu-id="93b0d-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="93b0d-132">为新资产创建相同金额的购置交易记录。</span><span class="sxs-lookup"><span data-stu-id="93b0d-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="93b0d-133">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="93b0d-133">Click Post.</span></span>


