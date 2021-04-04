---
title: 创建呼叫中心订单
description: 此程序会逐步演示如何查找客户，创建新订单，检索产品和收取客户的付款。
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ecf6fe97287fcfb3c070215b563542878175789c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264276"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="ad3fe-103">创建呼叫中心订单</span><span class="sxs-lookup"><span data-stu-id="ad3fe-103">Create call center orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad3fe-104">此程序会逐步演示如何查找客户，创建新订单，检索产品和收取客户的付款。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="ad3fe-105">此程序使用演示数据公司 USRT，旨在供销售订单职员使用。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="ad3fe-106">先决条件：完成此过程的用户被设置为呼叫中心用户，并且使用至少一个源代码发布 Fabrikam 半年目录。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="ad3fe-107">转到 **Retail 和 Commerce \> 客户 \> 客户服务**。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-107">Go to **Retail and Commerce \> Customers \> Customer service**.</span></span>
2. <span data-ttu-id="ad3fe-108">对于 **SearchText**，输入搜索条件以查找客户。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-108">For **SearchText**, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="ad3fe-109">对于此示例过程，输入“Karen”，然后选择 **选项卡**。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-109">For this example procedure, enter "Karen" and select **Tab**.</span></span>  
3. <span data-ttu-id="ad3fe-110">选择搜索。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-110">Select Search.</span></span>
    * <span data-ttu-id="ad3fe-111">由于演示数据中仅有一名客户的姓名是“Karen”，因此将自动选中。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-111">Since there is only one customer named "Karen" in demo data, the result will be automatically selected.</span></span>  
4. <span data-ttu-id="ad3fe-112">选择 **新建销售订单**。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-112">Select **New sales order**.</span></span>
5. <span data-ttu-id="ad3fe-113">展开或折叠 **销售订单** 标题部分。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-113">Expand or collapse the **Sales order** header section.</span></span>
6. <span data-ttu-id="ad3fe-114">选择目录的源代码。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="ad3fe-115">如果没有活动源代码，您可以跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-115">If there are no active source codes you can skip this step.</span></span>  
7. <span data-ttu-id="ad3fe-116">选择 **添加行**。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-116">Select **Add line**.</span></span>
8. <span data-ttu-id="ad3fe-117">对于 **物料编号**，输入物料搜索词。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-117">For **Item number**, enter the item search term.</span></span>
    * <span data-ttu-id="ad3fe-118">对于此示例过程，输入部分物料编号“8111”并按下选项卡。此操作将显示物料搜索窗口。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-118">For this sample procedure, enter a partial item number of '8111' and press tab. This action will bring up the item search window.</span></span>  
9. <span data-ttu-id="ad3fe-119">选择要添加到销售订单的产品。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-119">Select the product to add to the sales order.</span></span>
10. <span data-ttu-id="ad3fe-120">输入销售数量。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="ad3fe-121">选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-121">Select **Create**.</span></span>
12. <span data-ttu-id="ad3fe-122">选择 **完成** 以捕获客户付款。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-122">Select **Complete** to capture the customer payment.</span></span>
13. <span data-ttu-id="ad3fe-123">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-123">Select **Add**.</span></span>
    * <span data-ttu-id="ad3fe-124">“添加”链接位于“付款”选项卡中。如果重叠，则扩展“付款”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="ad3fe-125">选择付款方式。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-125">Select the payment method.</span></span>
    * <span data-ttu-id="ad3fe-126">对于此程序，选择现金付款方法。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="ad3fe-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-127">Close the page.</span></span>
16. <span data-ttu-id="ad3fe-128">输入金额。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-128">Enter the amount.</span></span>
    * <span data-ttu-id="ad3fe-129">对于此过程，输入与订单余额相等的金额，可在“销售订单摘要”页面的金额字段左侧看到订单余额。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-129">For this procedure, enter an amount equal to the order balance that can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="ad3fe-130">此操作将允许您以全额付清形式完成订单。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-130">This action will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="ad3fe-131">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-131">Select **OK**.</span></span>
18. <span data-ttu-id="ad3fe-132">选择 **提交**。</span><span class="sxs-lookup"><span data-stu-id="ad3fe-132">Select **Submit**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad3fe-133">其他资源</span><span class="sxs-lookup"><span data-stu-id="ad3fe-133">Additional resources</span></span>

[<span data-ttu-id="ad3fe-134">按交货方式自定义事务电子邮件</span><span class="sxs-lookup"><span data-stu-id="ad3fe-134">Customize transactional emails by mode of delivery</span></span>](../customize-email-delivery-mode.md)

[<span data-ttu-id="ad3fe-135">在 POS 上更改交货方式</span><span class="sxs-lookup"><span data-stu-id="ad3fe-135">Change mode of delivery in POS</span></span>](../pos-change-delivery-mode.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]