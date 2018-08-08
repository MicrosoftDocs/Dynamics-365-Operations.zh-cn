--- 
title: "设置销售税结算期间"
description: "销售税结算期间含有有关需要申报和缴纳的销售税的期间间隔的信息。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: d30a3271114574d2776921fb31b360389a1b3466
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="9b1d8-103">设置销售税结算期间</span><span class="sxs-lookup"><span data-stu-id="9b1d8-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9b1d8-104">销售税结算期间含有有关需要申报和缴纳的销售税的期间间隔的信息。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="9b1d8-105">结算流程可在结算期间或特定日期间隔内运行。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="9b1d8-106">所有与结算期间相关的税务代码将进行结算。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="9b1d8-107">根据相关销售税主管机构的设置，应交税金过帐到供应商或总帐科目。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="9b1d8-108">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="9b1d8-109">转到“纳税”>“间接税”>“销售税”>“销售税结算期间”。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="9b1d8-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-110">Click New.</span></span>
3. <span data-ttu-id="9b1d8-111">在“结算期间”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="9b1d8-112">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9b1d8-113">在“主管机构”字段中，选择接收为结算期间创建的报表和付款的销售税主管机构。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="9b1d8-114">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9b1d8-115">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9b1d8-116">在“付款”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9b1d8-117">相关销售税主管机构可以设置为供应商，销售税结算将创建开放式供应商发票。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="9b1d8-118">付款期限定义开放式供应商发票的到期日期。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="9b1d8-119">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="9b1d8-120">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="9b1d8-121">为结算期间间隔选择类型。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="9b1d8-122">输入每一期间的期间间隔单位数。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="9b1d8-123">例如，1 个季度有 3 个月。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="9b1d8-124">选择或清除销售税清算复选框上的“使用批处理”。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="9b1d8-125">结算期的结算流程可在后台将交易记录作为批处理作业。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="9b1d8-126">这是对在期间间隔内的大量涉税交易记录的建议。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
14. <span data-ttu-id="9b1d8-127">展开“期间间隔”选项卡。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-127">Expand the Period intervals tab.</span></span>
15. <span data-ttu-id="9b1d8-128">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-128">Click Add.</span></span>
16. <span data-ttu-id="9b1d8-129">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-129">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="9b1d8-130">在“开始日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-130">In the From date field, enter a date.</span></span>
18. <span data-ttu-id="9b1d8-131">在“结束日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-131">In the To date field, enter a date.</span></span>
19. <span data-ttu-id="9b1d8-132">单击“新建期间间隔”。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-132">Click New period interval.</span></span>
    * <span data-ttu-id="9b1d8-133">一旦输入第一个期间间隔，可自动创建新期间。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="9b1d8-134">您可以返回和根据需要添加新期间间隔。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-134">You can come back and add new period intervals as required.</span></span>  
20. <span data-ttu-id="9b1d8-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9b1d8-135">Close the page.</span></span>


