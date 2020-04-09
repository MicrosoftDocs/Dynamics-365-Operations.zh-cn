---
title: 零售价调整
description: 此程序将逐步演示如何创建商业价格调整。
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83498fa0a0432cb182106d6d273cb6117ed0b094
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141228"
---
# <a name="retail-price-adjustments"></a><span data-ttu-id="0ca7d-103">零售价调整</span><span class="sxs-lookup"><span data-stu-id="0ca7d-103">Retail price adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ca7d-104">此程序将逐步演示如何创建商业价格调整。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-104">This procedure will walk through creating a commerce price adjustment.</span></span> <span data-ttu-id="0ca7d-105">价格调整可以直接设置某一商品的销售价格，或修改其基础销售价格或贸易协议销售价格。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-105">A price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="0ca7d-106">此程序使用 USRT 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="0ca7d-107">单击“价格和折扣管理”。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="0ca7d-108">单击“价格调整”选项卡。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="0ca7d-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-109">Click New.</span></span>
    * <span data-ttu-id="0ca7d-110">您可在此创建所有最常用的价格和折扣规则，包括折扣、价格调整、贸易协议日记帐和类别定价规则。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-110">From here you can create all of the most commonly used price and discount rules, including discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="0ca7d-111">单击“价格调整”。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="0ca7d-112">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="0ca7d-113">展开“行”部分。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="0ca7d-114">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-114">Click Add.</span></span>
    * <span data-ttu-id="0ca7d-115">在本示例中，在“产品”字段中输入“81126”。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-115">For this example, enter '81126' in the Product field.</span></span> <span data-ttu-id="0ca7d-116">然后，在“折扣百分比”字段中，输入“10.0”。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="0ca7d-117">折扣百分比类型价格调整将会降低基础销售价格或贸易协议销售价格。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="0ca7d-118">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-118">Click Add.</span></span>
    * <span data-ttu-id="0ca7d-119">在本示例中，在“产品”字段中输入“81125”。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-119">For this example, enter '81125' in the Product field.</span></span> <span data-ttu-id="0ca7d-120">然后，选择“折扣方法”字段中的“现金折扣金额”。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="0ca7d-121">最后，在“现金折扣金额”字段中输入“5.0”。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="0ca7d-122">现金折扣金额折扣类型是从基础价或贸易协议价格减去的金额。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="0ca7d-123">单击“价格组”。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-123">Click Price groups.</span></span>
    * <span data-ttu-id="0ca7d-124">选择“价格组”字段中的“RP-休斯敦”。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="0ca7d-125">这将价格调整和休斯敦商店关联起来。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="0ca7d-126">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-126">Click Save.</span></span>
11. <span data-ttu-id="0ca7d-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-127">Close the page.</span></span>
12. <span data-ttu-id="0ca7d-128">在“状态”字段中，选择“已启用”。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="0ca7d-129">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-129">Click Save.</span></span>
14. <span data-ttu-id="0ca7d-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-130">Close the page.</span></span>
15. <span data-ttu-id="0ca7d-131">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="0ca7d-131">Refresh the page.</span></span>

