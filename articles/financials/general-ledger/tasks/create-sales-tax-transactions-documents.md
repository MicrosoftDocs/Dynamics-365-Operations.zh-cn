--- 
title: "在单据中创建销售税交易记录"
description: "单据上的销售税通过在单据行上提供销售税组和物料销售税组计算。"
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 27bf4ba33bd7d22443512d072572b9b1ffc164fa
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="f62c3-103">在单据中创建销售税交易记录</span><span class="sxs-lookup"><span data-stu-id="f62c3-103">Create sales tax transactions on documents</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f62c3-104">单据上的销售税通过在单据行上提供销售税组和物料销售税组计算。</span><span class="sxs-lookup"><span data-stu-id="f62c3-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="f62c3-105">这些默认显示主数据，但可以根据需要手动更改。</span><span class="sxs-lookup"><span data-stu-id="f62c3-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="f62c3-106">计算出的销售税可在行和单据中选中。</span><span class="sxs-lookup"><span data-stu-id="f62c3-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="f62c3-107">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="f62c3-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="f62c3-108">转到应收帐项目>订单>所有销售订单。</span><span class="sxs-lookup"><span data-stu-id="f62c3-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="f62c3-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f62c3-109">Click New.</span></span>
3. <span data-ttu-id="f62c3-110">在“客户帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f62c3-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f62c3-111">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f62c3-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f62c3-112">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f62c3-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f62c3-113">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f62c3-113">Click OK.</span></span>
7. <span data-ttu-id="f62c3-114">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="f62c3-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="f62c3-115">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f62c3-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="f62c3-116">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f62c3-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="f62c3-117">在“单价”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f62c3-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="f62c3-118">展开或折叠“行详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="f62c3-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="f62c3-119">单击“设置”选项卡。</span><span class="sxs-lookup"><span data-stu-id="f62c3-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="f62c3-120">在“物料销售税组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f62c3-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="f62c3-121">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f62c3-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="f62c3-122">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f62c3-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="f62c3-123">单击“财务”。</span><span class="sxs-lookup"><span data-stu-id="f62c3-123">Click Financials.</span></span>
17. <span data-ttu-id="f62c3-124">单击“销售税”。</span><span class="sxs-lookup"><span data-stu-id="f62c3-124">Click Sales tax.</span></span>
18. <span data-ttu-id="f62c3-125">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f62c3-125">Click OK.</span></span>
19. <span data-ttu-id="f62c3-126">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="f62c3-126">Click Add line.</span></span>
20. <span data-ttu-id="f62c3-127">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="f62c3-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="f62c3-128">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f62c3-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="f62c3-129">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f62c3-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="f62c3-130">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f62c3-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="f62c3-131">在“单价”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f62c3-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="f62c3-132">在“物料销售税组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f62c3-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="f62c3-133">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f62c3-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="f62c3-134">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f62c3-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="f62c3-135">在操作窗格上，单击“销售”。</span><span class="sxs-lookup"><span data-stu-id="f62c3-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="f62c3-136">单击“销售税”。</span><span class="sxs-lookup"><span data-stu-id="f62c3-136">Click Sales tax.</span></span>
30. <span data-ttu-id="f62c3-137">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f62c3-137">Click OK.</span></span>


