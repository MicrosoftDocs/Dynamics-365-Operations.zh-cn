---
title: 创建贸易协议使用的类别定价规则
description: 该过程说明了如何使用分类价格规则创建销售价格贸易协议。
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPricingDiscountCategoryPriceRule, RetailCategoryPriceRule, EcoResCategorySingleLookup, RetailCategoryPriceWizard, PriceDiscAdm, PriceDiscAdmTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21b1986aa36aab23f50a5af434435f9e93318e45
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410544"
---
# <a name="category-pricing-rules-to-create-trade-agreements"></a><span data-ttu-id="6565f-103">创建贸易协议使用的类别定价规则</span><span class="sxs-lookup"><span data-stu-id="6565f-103">Category pricing rules to create trade agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6565f-104">该过程说明了如何使用分类价格规则创建销售价格贸易协议。</span><span class="sxs-lookup"><span data-stu-id="6565f-104">This procedure demonstrates how to create sales price trade agreements using a category pricing rule.</span></span> <span data-ttu-id="6565f-105">创建此任务的演示数据公司是 USRT。</span><span class="sxs-lookup"><span data-stu-id="6565f-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="6565f-106">此任务目的在于供商业推销经理角色使用。</span><span class="sxs-lookup"><span data-stu-id="6565f-106">This task is intended for the Commerce merchandising manager role.</span></span>

1. <span data-ttu-id="6565f-107">单击“价格和折扣管理”。</span><span class="sxs-lookup"><span data-stu-id="6565f-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="6565f-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="6565f-108">Click New.</span></span>
3. <span data-ttu-id="6565f-109">单击“分类价格规则”。</span><span class="sxs-lookup"><span data-stu-id="6565f-109">Click Category price rule.</span></span>
4. <span data-ttu-id="6565f-110">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="6565f-110">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="6565f-111">在“帐户代码”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="6565f-111">In the Account code field, select an option.</span></span>
    * <span data-ttu-id="6565f-112">一个“组”类型帐户代码用于设置销售价格贸易协议，由销售渠道、积分项目、产品目录以及附属关系等具体细节组成。</span><span class="sxs-lookup"><span data-stu-id="6565f-112">A "Group" type account code is used to set up sales price trade agreements that are specific for Channels, Loyalty programs, Catalogs, and Affiliations.</span></span>  
6. <span data-ttu-id="6565f-113">在“帐户部分”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="6565f-113">In the Account selection field, enter or select a value.</span></span>
7. <span data-ttu-id="6565f-114">在“分类”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="6565f-114">In the Category field, enter or select a value.</span></span>
8. <span data-ttu-id="6565f-115">在“金额/百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="6565f-115">In the Amount/Percent field, enter a number.</span></span>
9. <span data-ttu-id="6565f-116">在“舍入版本”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="6565f-116">In the Rounding version field, enter or select a value.</span></span>
10. <span data-ttu-id="6565f-117">单击“生成贸易协议”。</span><span class="sxs-lookup"><span data-stu-id="6565f-117">Click Generate trade agreements.</span></span>
11. <span data-ttu-id="6565f-118">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="6565f-118">Click Next.</span></span>
12. <span data-ttu-id="6565f-119">在“开始日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="6565f-119">In the From date field, enter a date.</span></span>
13. <span data-ttu-id="6565f-120">在“结束日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="6565f-120">In the To date field, enter a date.</span></span>
14. <span data-ttu-id="6565f-121">在“查找下一个”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="6565f-121">Select Yes in the Find next field.</span></span>
15. <span data-ttu-id="6565f-122">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="6565f-122">Click Next.</span></span>
16. <span data-ttu-id="6565f-123">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="6565f-123">Click Finish.</span></span>
    * <span data-ttu-id="6565f-124">由此创建一个“贸易协议日记帐”并打开预览。</span><span class="sxs-lookup"><span data-stu-id="6565f-124">This creates a Trade agreement journal and opens it for your review.</span></span>  
17. <span data-ttu-id="6565f-125">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6565f-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6565f-126">该贸易协议日记帐是根据未发布的“分类价格规则”创建的。</span><span class="sxs-lookup"><span data-stu-id="6565f-126">The trade agreement journals created from the Category pricing rules aren't posted.</span></span> <span data-ttu-id="6565f-127">在发布之前，可以预览并修改所生成的价格。</span><span class="sxs-lookup"><span data-stu-id="6565f-127">You can  review and edit the prices generated before posting them.</span></span>  
18. <span data-ttu-id="6565f-128">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="6565f-128">Click Edit.</span></span>
19. <span data-ttu-id="6565f-129">在“货币金额”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="6565f-129">In the Amount in currency field, enter a number.</span></span>
20. <span data-ttu-id="6565f-130">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="6565f-130">Click Post.</span></span>
21. <span data-ttu-id="6565f-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6565f-131">Click OK.</span></span>
22. <span data-ttu-id="6565f-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6565f-132">Close the page.</span></span>
23. <span data-ttu-id="6565f-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6565f-133">Close the page.</span></span>
24. <span data-ttu-id="6565f-134">单击“分类价格规则”选项卡。</span><span class="sxs-lookup"><span data-stu-id="6565f-134">Click the Category price rules tab.</span></span>
    * <span data-ttu-id="6565f-135">此列表列明了销售渠道的具体“分类价格规则”。</span><span class="sxs-lookup"><span data-stu-id="6565f-135">Channel specific Category pricing rules will show in this list.</span></span>  

