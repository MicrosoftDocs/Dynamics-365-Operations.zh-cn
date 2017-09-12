--- 
title: "创建呼叫中心订单"
description: "此程序会逐步演示如何查找客户，创建新订单，检索产品和收取客户的付款。"
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 62f88cc2e28405a9d2eb43819fb09d83a64658b6
ms.contentlocale: zh-cn
ms.lasthandoff: 07/28/2017

---
# <a name="create-call-center-orders"></a><span data-ttu-id="f8c2c-103">创建呼叫中心订单</span><span class="sxs-lookup"><span data-stu-id="f8c2c-103">Create call center orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f8c2c-104">此程序会逐步演示如何查找客户，创建新订单，检索产品和收取客户的付款。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="f8c2c-105">此程序使用演示数据公司 USRT，旨在供销售订单职员使用。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="f8c2c-106">先决条件：完成此过程的用户被设置为呼叫中心用户，并且使用至少一个源代码发布 Fabrikam 半年目录。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="f8c2c-107">转至“零售和商业”>“客户”>“客户服务”。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="f8c2c-108">在 SearchText 字段中，输入检索条件以查找客户。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-108">In the SearchText field, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="f8c2c-109">对于此示例程序，键入“Karen”，然后按下选项卡。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-109">For this example procedure type in 'karen' and press tab.</span></span>  
3. <span data-ttu-id="f8c2c-110">单击“搜索”。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-110">Click Search.</span></span>
    * <span data-ttu-id="f8c2c-111">由于演示数据中仅有一名客户的姓名是 Karen，因此它们将被自动选中。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-111">Since there is only one customer named Karen in demo data they will be automatically selected.</span></span>  
4. <span data-ttu-id="f8c2c-112">单击“新建销售订单”。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-112">Click New sales order.</span></span>
5. <span data-ttu-id="f8c2c-113">扩展或折叠“销售订单标题”部分。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-113">Expand or collapse the Sales order header section.</span></span>
6. <span data-ttu-id="f8c2c-114">选择目录的源代码。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="f8c2c-115">如果没有活动源代码，您可以关闭源字段并跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-115">If there are no active Source codes you can close the Source field and skip this step.</span></span>  
7. <span data-ttu-id="f8c2c-116">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-116">Click Add line.</span></span>
8. <span data-ttu-id="f8c2c-117">在“物料编号”字段中，输入物料搜索词。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-117">In the Item number field, enter the item search term.</span></span>
    * <span data-ttu-id="f8c2c-118">对于此示例过程，输入部分物料编号“8111”并按下选项卡。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-118">For this sample procedure enter a partial item number of '8111' and press tab.</span></span> <span data-ttu-id="f8c2c-119">这将弹出物料检索窗口。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-119">This will pop up the item search window.</span></span>  
9. <span data-ttu-id="f8c2c-120">选择产品以添加到销售订单</span><span class="sxs-lookup"><span data-stu-id="f8c2c-120">Select the product to add to the sales order</span></span>
10. <span data-ttu-id="f8c2c-121">输入销售数量。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-121">Enter the sales quantity.</span></span>
11. <span data-ttu-id="f8c2c-122">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-122">Click Create.</span></span>
12. <span data-ttu-id="f8c2c-123">单击“完成”以获取客户付款。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-123">Click Complete to capture the customer payment.</span></span>
13. <span data-ttu-id="f8c2c-124">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-124">Click Add.</span></span>
    * <span data-ttu-id="f8c2c-125">“添加”链接位于“付款”选项卡中。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-125">The Add link is in the Payments tab.</span></span> <span data-ttu-id="f8c2c-126">如果重叠，则扩展“付款”选项卡。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-126">Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="f8c2c-127">选择付款方式。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-127">Select the payment method.</span></span>
    * <span data-ttu-id="f8c2c-128">对于此程序，选择现金付款方法。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-128">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="f8c2c-129">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-129">Close the page.</span></span>
16. <span data-ttu-id="f8c2c-130">输入金额。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-130">Enter the amount.</span></span>
    * <span data-ttu-id="f8c2c-131">对于此程序，输入与订单余额相等的金额，订单余额可在“销售订单摘要”页面的金额字段左侧看到。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-131">For this procedure enter an amount equal to the order balance which can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="f8c2c-132">这将允许您以全部付讫形式完成订单。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-132">This will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="f8c2c-133">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-133">Click OK.</span></span>
18. <span data-ttu-id="f8c2c-134">单击“提交”。</span><span class="sxs-lookup"><span data-stu-id="f8c2c-134">Click Submit.</span></span>


