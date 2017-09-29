--- 
title: "从应付帐款创建和购置资产"
description: "本指到任务帮助了解如何遵照采购流程来创建和购置固定资产。 "
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c483622346bf61d0805402ae4ae8d2ba7c7aed89
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="d765d-103">从应付帐款创建和购置资产</span><span class="sxs-lookup"><span data-stu-id="d765d-103">Create and acquire assets from accounts payable</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d765d-104">本指到任务帮助了解如何遵照采购流程来创建和购置固定资产。 </span><span class="sxs-lookup"><span data-stu-id="d765d-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="d765d-105">本任务需要用到普通及应付账目会计和演示公司USMF的数据。</span><span class="sxs-lookup"><span data-stu-id="d765d-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="d765d-106">设置固定资产参数</span><span class="sxs-lookup"><span data-stu-id="d765d-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="d765d-107">转到固定资产>设置>固定资产参数。</span><span class="sxs-lookup"><span data-stu-id="d765d-107">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="d765d-108">展开或折叠“采购订单”部分。</span><span class="sxs-lookup"><span data-stu-id="d765d-108">Expand or collapse the Purchase orders section.</span></span>
3. <span data-ttu-id="d765d-109">勾选“允许从采购中购置资产”复选框。</span><span class="sxs-lookup"><span data-stu-id="d765d-109">Check the Allow asset acquisition from Purchasing checkbox.</span></span>
4. <span data-ttu-id="d765d-110">勾选“在产品收据或发票过帐期间创建资产”复选框。</span><span class="sxs-lookup"><span data-stu-id="d765d-110">Check the Create asset during product receipt or invoice posting checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="d765d-111">创建新的供应商发票</span><span class="sxs-lookup"><span data-stu-id="d765d-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="d765d-112">转到“应付帐款”>“工作区”>“供应商发票条目”。</span><span class="sxs-lookup"><span data-stu-id="d765d-112">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="d765d-113">单击“新建供应商发票”。</span><span class="sxs-lookup"><span data-stu-id="d765d-113">Click New vendor invoice.</span></span>
3. <span data-ttu-id="d765d-114">在“发票帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="d765d-114">In the Invoice account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d765d-115">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d765d-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d765d-116">在“编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d765d-116">In the Number field, type a value.</span></span>
6. <span data-ttu-id="d765d-117">在“过帐日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="d765d-117">In the Posting date field, enter a date.</span></span>
7. <span data-ttu-id="d765d-118">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="d765d-118">Click Add line.</span></span>
8. <span data-ttu-id="d765d-119">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="d765d-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d765d-120">输入固定资产购置时可使用的非贮存物料或采购类别。</span><span class="sxs-lookup"><span data-stu-id="d765d-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="d765d-121">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d765d-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="d765d-122">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d765d-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="d765d-123">一个发票行只创建一哥固定资产，不考虑数量。</span><span class="sxs-lookup"><span data-stu-id="d765d-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span>  <span data-ttu-id="d765d-124">发票数量字段的值会被传送到固定资产数量参数</span><span class="sxs-lookup"><span data-stu-id="d765d-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="d765d-125">在“单位价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d765d-125">In the Unit price field, enter a number.</span></span>
12. <span data-ttu-id="d765d-126">展开或折叠“行详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="d765d-126">Expand or collapse the Line details section.</span></span>
13. <span data-ttu-id="d765d-127">单击“固定资产”选项卡。</span><span class="sxs-lookup"><span data-stu-id="d765d-127">Click the Fixed assets tab.</span></span>
14. <span data-ttu-id="d765d-128">选中“创建新的固定资产”复选框。</span><span class="sxs-lookup"><span data-stu-id="d765d-128">Check the Create a new fixed asset checkbox.</span></span>
15. <span data-ttu-id="d765d-129">在“固定资产组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="d765d-129">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="d765d-130">在列表中，选择创建新固定资产时要使用的固定资产组。</span><span class="sxs-lookup"><span data-stu-id="d765d-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="d765d-131">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d765d-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="d765d-132">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="d765d-132">Click Post.</span></span>
    * <span data-ttu-id="d765d-133">在过帐发票时，将会创建和购置固定资产。</span><span class="sxs-lookup"><span data-stu-id="d765d-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  


