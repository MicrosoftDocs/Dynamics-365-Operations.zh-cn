---
title: 创建新的贸易协议
description: 该过程会显示如何创建贸易协议，您可在其中登记您与特定客户达成的新产品销售价格。
author: omulvad
manager: AnnBe
ms.date: 11/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e132cd20437b7929e81fcaa123d70bb57fb320c8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549259"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="f280f-103">创建新的贸易协议</span><span class="sxs-lookup"><span data-stu-id="f280f-103">Create a new trade agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f280f-104">该过程会显示如何创建贸易协议，您可在其中登记您与特定客户达成的新产品销售价格。</span><span class="sxs-lookup"><span data-stu-id="f280f-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="f280f-105">您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="f280f-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="f280f-106">如果您正在使用您自己的数据，在您开始本指南之前，您需要确保贸易协议日记帐名称存在，且其中的默认关系被设置为“价格（售价）”。</span><span class="sxs-lookup"><span data-stu-id="f280f-106">If you’re using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to “Price (sales)”.</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="f280f-107">创建和发表新的贸易协议日记帐</span><span class="sxs-lookup"><span data-stu-id="f280f-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="f280f-108">转至“销售和营销”>“价格和折扣”>“贸易协议日记帐”。</span><span class="sxs-lookup"><span data-stu-id="f280f-108">Go to Sales and marketing > Prices and discounts > Trade agreement journals.</span></span>
2. <span data-ttu-id="f280f-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f280f-109">Click New.</span></span>
3. <span data-ttu-id="f280f-110">在“名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f280f-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f280f-111">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f280f-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f280f-112">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f280f-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f280f-113">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="f280f-113">Click Lines.</span></span>
7. <span data-ttu-id="f280f-114">在“帐户代码”字段中，选择“表格”。</span><span class="sxs-lookup"><span data-stu-id="f280f-114">In the Account code field, select 'Table'.</span></span>
    * <span data-ttu-id="f280f-115">在此示例中，您正在更新特定客户的价格，这意味着您需要选择表格。</span><span class="sxs-lookup"><span data-stu-id="f280f-115">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="f280f-116">如果您正在更新产品的目录价格，您可以选择“全部”，如此新价格将对所有客户有效。</span><span class="sxs-lookup"><span data-stu-id="f280f-116">If you were updating the product's list price, you would select All, so that the new price is valid for all customers.</span></span> <span data-ttu-id="f280f-117">如果您正在区分不同客户细分的价格，则您可以选择组。</span><span class="sxs-lookup"><span data-stu-id="f280f-117">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="f280f-118">若要选择“组”，您必须设置“客户价格组”。</span><span class="sxs-lookup"><span data-stu-id="f280f-118">To select Group, you must have set up Customer price groups.</span></span>  
8. <span data-ttu-id="f280f-119">在“帐户选择”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f280f-119">In the Account selection field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="f280f-120">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f280f-120">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="f280f-121">在“物料”字段中，选择“表格”。</span><span class="sxs-lookup"><span data-stu-id="f280f-121">In the Item code field, select 'Table'.</span></span>
    * <span data-ttu-id="f280f-122">在输入贸易协议类型“价格（售价）”时，您仅可选择“物料代码”字段中的“表格”。</span><span class="sxs-lookup"><span data-stu-id="f280f-122">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the Item code field.</span></span> <span data-ttu-id="f280f-123">原因在于价格是绝对值，所有产品或一组产品的价格不能完成相同。</span><span class="sxs-lookup"><span data-stu-id="f280f-123">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>  
11. <span data-ttu-id="f280f-124">在“物料关系”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f280f-124">In the Item relation field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="f280f-125">在列表中，选择您想要包括在协议中的产品。</span><span class="sxs-lookup"><span data-stu-id="f280f-125">In the list, select the product you want to include in the agreement.</span></span>
    * <span data-ttu-id="f280f-126">记下您已选中的产品。</span><span class="sxs-lookup"><span data-stu-id="f280f-126">Make a note of which product you've selected.</span></span>  
13. <span data-ttu-id="f280f-127">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f280f-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="f280f-128">在“从”字段中，输入最小数量。</span><span class="sxs-lookup"><span data-stu-id="f280f-128">In the From field, enter a minimum quantity.</span></span>
    * <span data-ttu-id="f280f-129">如果客户必须订购最小数量的产品，然后才能有资格获得新价格，则您需要在此指定最小数量。</span><span class="sxs-lookup"><span data-stu-id="f280f-129">If the customer has to order a minimum quantity  before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    * <span data-ttu-id="f280f-130">在“至”字段中输入一个值以指定最大数量，高于该数量的协议价格将无效。</span><span class="sxs-lookup"><span data-stu-id="f280f-130">Enter a value in the To field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="f280f-131">如果您基于多个数量分段提供价格和折扣，则指定每个数量等级段为一对最小和最大数量，分别在“从”和“至”字段中输入最小数量和最大数量。</span><span class="sxs-lookup"><span data-stu-id="f280f-131">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the 'From' and 'To' fields respectively.</span></span>  
15. <span data-ttu-id="f280f-132">在“货币金额”字段中，输入价格。</span><span class="sxs-lookup"><span data-stu-id="f280f-132">In the Amount in currency field, enter a price.</span></span>
16. <span data-ttu-id="f280f-133">在“开始日期”字段中，输入本协议开始生效的日期。</span><span class="sxs-lookup"><span data-stu-id="f280f-133">In the From date field, enter a date from which this agreement will be valid.</span></span>
17. <span data-ttu-id="f280f-134">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f280f-134">Click Save.</span></span>
18. <span data-ttu-id="f280f-135">单击“验证”。</span><span class="sxs-lookup"><span data-stu-id="f280f-135">Click Validate.</span></span>
19. <span data-ttu-id="f280f-136">单击“验证”选定的行。</span><span class="sxs-lookup"><span data-stu-id="f280f-136">Click Validate selected lines.</span></span>
20. <span data-ttu-id="f280f-137">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f280f-137">Click OK.</span></span>
21. <span data-ttu-id="f280f-138">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="f280f-138">Click Post.</span></span>
22. <span data-ttu-id="f280f-139">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f280f-139">Click OK.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="f280f-140">查看某一产品的贸易协议</span><span class="sxs-lookup"><span data-stu-id="f280f-140">View trade agreements for a product</span></span>
1. <span data-ttu-id="f280f-141">转到“产品信息管理”>“产品”>“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="f280f-141">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="f280f-142">在列表中，查找并选择您刚更新价格的产品。</span><span class="sxs-lookup"><span data-stu-id="f280f-142">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="f280f-143">在“操作窗格”上，单击“销售”。</span><span class="sxs-lookup"><span data-stu-id="f280f-143">On the Action Pane, click Sell.</span></span>
4. <span data-ttu-id="f280f-144">单击“查看贸易协议”。</span><span class="sxs-lookup"><span data-stu-id="f280f-144">Click View trade agreements.</span></span>
    * <span data-ttu-id="f280f-145">审查您刚创建的价格贸易协议的详情。</span><span class="sxs-lookup"><span data-stu-id="f280f-145">Review the details of the price trade agreement you have just created.</span></span>    
5. <span data-ttu-id="f280f-146">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f280f-146">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f280f-147">其他资源</span><span class="sxs-lookup"><span data-stu-id="f280f-147">Additional resources</span></span>
### <a name="community-blogs"></a><span data-ttu-id="f280f-148">社区博客</span><span class="sxs-lookup"><span data-stu-id="f280f-148">Community blogs</span></span>
- [<span data-ttu-id="f280f-149">Dynamics 365 for Finance and Operations 中的销售价</span><span class="sxs-lookup"><span data-stu-id="f280f-149">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
