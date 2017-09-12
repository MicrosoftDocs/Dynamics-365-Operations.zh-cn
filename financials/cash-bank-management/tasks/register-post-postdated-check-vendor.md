--- 
title: "为供应商登记和过帐远期支票"
description: "在通过使用日记帐凭证给供应商签发支票之前，先注册远期支票的详细信息。"
author: kweekley
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
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8689421d3281f93af9298f777f92c5c3b2c1c86c
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="473d1-103">为供应商登记和过帐远期支票</span><span class="sxs-lookup"><span data-stu-id="473d1-103">Register and post a postdated check for a vendor</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="473d1-104">在通过使用日记帐凭证给供应商签发支票之前，先注册远期支票的详细信息。</span><span class="sxs-lookup"><span data-stu-id="473d1-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="473d1-105">您还可以过帐该远期发票并生成财务交易记录。</span><span class="sxs-lookup"><span data-stu-id="473d1-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="473d1-106">在注册并过帐远期支票给供应商之前，请完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="473d1-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="473d1-107">在“现金和银行管理”页设置远期支票。</span><span class="sxs-lookup"><span data-stu-id="473d1-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="473d1-108">此任务指南的角色是出纳员。</span><span class="sxs-lookup"><span data-stu-id="473d1-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="473d1-109">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="473d1-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="473d1-110">转到“应付帐款”>“付款”>“付款日记帐”</span><span class="sxs-lookup"><span data-stu-id="473d1-110">Go to Acounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="473d1-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="473d1-111">Click New.</span></span>
3. <span data-ttu-id="473d1-112">在“名称”字段中，键入“VendPay”。</span><span class="sxs-lookup"><span data-stu-id="473d1-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="473d1-113">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="473d1-113">Click Lines.</span></span>
5. <span data-ttu-id="473d1-114">在“帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="473d1-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="473d1-115">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="473d1-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="473d1-116">在“借方”字段中，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="473d1-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="473d1-117">在“付款方式”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="473d1-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="473d1-118">选择远期支票的付款方式。</span><span class="sxs-lookup"><span data-stu-id="473d1-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="473d1-119">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="473d1-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="473d1-120">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="473d1-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="473d1-121">单击“远期支票”选项卡。</span><span class="sxs-lookup"><span data-stu-id="473d1-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="473d1-122">在“支票号码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="473d1-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="473d1-123">输入或更改远期支票的数目。</span><span class="sxs-lookup"><span data-stu-id="473d1-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="473d1-124">在“开证银行名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="473d1-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="473d1-125">输入签发银行的银行详细资料。</span><span class="sxs-lookup"><span data-stu-id="473d1-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="473d1-126">单击“列表”选项卡。</span><span class="sxs-lookup"><span data-stu-id="473d1-126">Click the List tab.</span></span>
15. <span data-ttu-id="473d1-127">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="473d1-127">Click Post.</span></span>
16. <span data-ttu-id="473d1-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="473d1-128">Close the page.</span></span>
17. <span data-ttu-id="473d1-129">单击“远期支票”选项卡。</span><span class="sxs-lookup"><span data-stu-id="473d1-129">Click the Postdated checks tab.</span></span>


