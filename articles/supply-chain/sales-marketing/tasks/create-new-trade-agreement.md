---
title: 创建新的贸易协议
description: 该过程会显示如何创建贸易协议，您可在其中登记您与特定客户达成的新产品销售价格。
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1e1b48531e7ef7d55774936cb71130d048cdab7
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830445"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="ad4a9-103">创建新的贸易协议</span><span class="sxs-lookup"><span data-stu-id="ad4a9-103">Create a new trade agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad4a9-104">该过程会显示如何创建贸易协议，您可在其中登记您与特定客户达成的新产品销售价格。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="ad4a9-105">您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="ad4a9-106">如果您正在使用您自己的数据，在您开始本指南之前，您需要确保贸易协议日记帐名称存在，且其中的默认关系被设置为“价格（售价）”。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-106">If you're using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to "Price (sales)".</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="ad4a9-107">创建和发表新的贸易协议日记帐</span><span class="sxs-lookup"><span data-stu-id="ad4a9-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="ad4a9-108">转到**导航窗格 > 模块 > 销售和营销 > 价格和折扣 > 贸易协议日记帐**。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-108">Go to **Navigation pane > Modules > Sales and marketing > Prices and discounts > Trade agreement journals**.</span></span>
2. <span data-ttu-id="ad4a9-109">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-109">Click **New**.</span></span>
3. <span data-ttu-id="ad4a9-110">在**名称**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-110">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ad4a9-111">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ad4a9-112">在**操作窗格**上，单击**行**。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-112">On **Action Pane**, click **Lines**.</span></span>
6. <span data-ttu-id="ad4a9-113">在**帐户代码**字段中，选择“表格”。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-113">In the **Account code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="ad4a9-114">在此示例中，您正在更新特定客户的价格，这意味着您需要选择表格。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-114">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="ad4a9-115">如果您正在更新产品的目录价格，您可以选择“全部”，如此新价格将对所有客户有效。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-115">If you were updating the product's list price, you would select 'All', so that the new price is valid for all customers.</span></span> <span data-ttu-id="ad4a9-116">如果您正在区分不同客户细分的价格，则您可以选择组。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-116">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="ad4a9-117">若要选择“组”，您必须设置“客户价格组”。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-117">To select Group, you must have set up Customer price groups.</span></span>  

7. <span data-ttu-id="ad4a9-118">在**帐户选择**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-118">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="ad4a9-119">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="ad4a9-120">在**物料代码**字段中，选择“表格”。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-120">In the **Item code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="ad4a9-121">在输入贸易协议类型“价格（销售额）”时，您仅可选择**物料代码**字段中的“表格”。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-121">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the **Item code** field.</span></span> <span data-ttu-id="ad4a9-122">原因在于价格是绝对值，所有产品或一组产品的价格不能完成相同。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-122">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>
    
10. <span data-ttu-id="ad4a9-123">在**物料关系**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-123">In the **Item relation** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="ad4a9-124">在列表中，选择您想要包括在协议中的产品。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-124">In the list, select the product you want to include in the agreement.</span></span> <span data-ttu-id="ad4a9-125">记下您已选中的产品。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-125">Make a note of which product you've selected.</span></span>  
12. <span data-ttu-id="ad4a9-126">在**从**字段中，输入最小数量。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-126">In the **From** field, enter a minimum quantity.</span></span>
    - <span data-ttu-id="ad4a9-127">如果客户必须订购最小数量的产品，然后才能有资格获得新价格，则您需要在此指定最小数量。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-127">If the customer has to order a minimum quantity before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    - <span data-ttu-id="ad4a9-128">在**至**字段中输入一个值以指定最大数量，高于该数量的协议价格将无效。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-128">Enter a value in the **To** field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="ad4a9-129">如果您基于多个数量分段提供价格和折扣，则指定每个数量等级段为一对最小和最大数量，分别在**从**和**至**字段中输入最小数量和最大数量。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-129">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the **From** and **To** fields respectively.</span></span>
13. <span data-ttu-id="ad4a9-130">在**货币金额**字段中，输入价格。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-130">In the **Amount in currency field**, enter a price.</span></span>
14. <span data-ttu-id="ad4a9-131">在**详细信息**部分下**开始日期**字段中，输入本协议开始生效的日期。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-131">Under the **Details** section, in the **From date** field, enter a date from which this agreement will be valid.</span></span>
15. <span data-ttu-id="ad4a9-132">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-132">Click **Save**.</span></span>
16. <span data-ttu-id="ad4a9-133">单击**验证**。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-133">Click **Validate**.</span></span>
17. <span data-ttu-id="ad4a9-134">单击**验证所选行**。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-134">Click **Validate selected lines**.</span></span>
18. <span data-ttu-id="ad4a9-135">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-135">Click **OK**.</span></span>
19. <span data-ttu-id="ad4a9-136">单击**过帐**。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-136">Click **Post**.</span></span>
20. <span data-ttu-id="ad4a9-137">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-137">Click **OK**.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="ad4a9-138">查看某一产品的贸易协议</span><span class="sxs-lookup"><span data-stu-id="ad4a9-138">View trade agreements for a product</span></span>
1. <span data-ttu-id="ad4a9-139">转到**导航窗格 > 模块 > 产品信息管理 > 产品 > 已发放产品**。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-139">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="ad4a9-140">在列表中，查找并选择您刚更新价格的产品。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-140">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="ad4a9-141">在**操作窗格**上，单击**销售**。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-141">On the **Action Pane**, click **Sell**.</span></span>
4. <span data-ttu-id="ad4a9-142">单击**查看贸易协议**。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-142">Click **View trade agreements**.</span></span>
    
    <span data-ttu-id="ad4a9-143">审查您刚创建的价格贸易协议的详情。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-143">Review the details of the price trade agreement you have just created.</span></span>    

5. <span data-ttu-id="ad4a9-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ad4a9-144">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad4a9-145">其他资源</span><span class="sxs-lookup"><span data-stu-id="ad4a9-145">Additional resources</span></span>
### <a name="community-blogs"></a><span data-ttu-id="ad4a9-146">社区博客</span><span class="sxs-lookup"><span data-stu-id="ad4a9-146">Community blogs</span></span>
- [<span data-ttu-id="ad4a9-147">Dynamics 365 for Finance and Operations 中的销售价</span><span class="sxs-lookup"><span data-stu-id="ad4a9-147">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
