--- 
title: "创建消耗量申请"
description: "该过程向您介绍创建申请的流程。"
author: mkirknel
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bad86a4726ce69015f318d9af98992b36d34b29a
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-requisition-for-consumption"></a><span data-ttu-id="2dc36-103">创建消耗量申请</span><span class="sxs-lookup"><span data-stu-id="2dc36-103">Create a requisition for consumption</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2dc36-104">该过程向您介绍创建申请的流程。</span><span class="sxs-lookup"><span data-stu-id="2dc36-104">This procedure walks you through the process of creating a requisition.</span></span> <span data-ttu-id="2dc36-105">它显示了在您的采购目录中搜索产品以及添加不在您目录中的产品的各种方法。</span><span class="sxs-lookup"><span data-stu-id="2dc36-105">It shows you different ways to search for products in your procurement catalog and how to add a product that isn’t in your catalog.</span></span> <span data-ttu-id="2dc36-106">在启动此过程前，必须将采购策略设置为申请默认类型为“消耗量”。</span><span class="sxs-lookup"><span data-stu-id="2dc36-106">Before you start this procedure, you must have a purchasing policy set up with Consumption as the default type of requisition.</span></span> <span data-ttu-id="2dc36-107">您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。</span><span class="sxs-lookup"><span data-stu-id="2dc36-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="2dc36-108">此过程只能由设置为工作人员的用户配置文件执行。</span><span class="sxs-lookup"><span data-stu-id="2dc36-108">The procedure can only be carried out by a user profile that is set up as worker.</span></span>  <span data-ttu-id="2dc36-109">此任务通常由员工完成。</span><span class="sxs-lookup"><span data-stu-id="2dc36-109">This task would normally be carried out by an employee.</span></span> <span data-ttu-id="2dc36-110">员工雇用安全角色可以使您执行任务，或者，如果您使用 USMF，您可以以Alicia身份登录。</span><span class="sxs-lookup"><span data-stu-id="2dc36-110">The Employee employ security role will allow you to carry out the tasks, or if you’re using USMF, you can log in as Alicia.</span></span>


## <a name="create-a-new-requisition"></a><span data-ttu-id="2dc36-111">新建申请</span><span class="sxs-lookup"><span data-stu-id="2dc36-111">Create a new requisition</span></span>
1. <span data-ttu-id="2dc36-112">转到“采购”>“采购申请”>“由我起草的采购申请”。</span><span class="sxs-lookup"><span data-stu-id="2dc36-112">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="2dc36-113">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="2dc36-113">Click New.</span></span>
3. <span data-ttu-id="2dc36-114">在“名称”字段中，为申请命名。</span><span class="sxs-lookup"><span data-stu-id="2dc36-114">In the Name field, give the requisition a name.</span></span>
4. <span data-ttu-id="2dc36-115">在“请求日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="2dc36-115">In the Requested date field, enter a date.</span></span>
    * <span data-ttu-id="2dc36-116">在默认情况下，请求的日期和会计结算日期会被复制到采购申请行。</span><span class="sxs-lookup"><span data-stu-id="2dc36-116">By default, the requested date and accounting date are copied to the purchase requisition lines.</span></span> <span data-ttu-id="2dc36-117">可以在行级别更改它们。</span><span class="sxs-lookup"><span data-stu-id="2dc36-117">They can be changed at the line level.</span></span> <span data-ttu-id="2dc36-118">请求日期是请求的交货日期。</span><span class="sxs-lookup"><span data-stu-id="2dc36-118">The requested date is the requested delivery date.</span></span>  
5. <span data-ttu-id="2dc36-119">在“会计结算日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="2dc36-119">In the Accounting date field, enter a date.</span></span>
    * <span data-ttu-id="2dc36-120">该核算日期用于在总帐中记录会计分录并验证预算资金是否可用。</span><span class="sxs-lookup"><span data-stu-id="2dc36-120">The accounting date is used to record the accounting entry in the general ledger, and to validate whether budget funds are available.</span></span>  
6. <span data-ttu-id="2dc36-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2dc36-121">Click OK.</span></span>
7. <span data-ttu-id="2dc36-122">在“原因”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="2dc36-122">In the Reason field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2dc36-123">默认情况下，您选择的业务理由原因会出现在采购申请行，但您可以在行级别更改它。</span><span class="sxs-lookup"><span data-stu-id="2dc36-123">By default, the business justification reason that you select appears for the purchase requisition lines, but you can change it at the line level.</span></span>    
8. <span data-ttu-id="2dc36-124">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="2dc36-124">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="2dc36-125">选择原因</span><span class="sxs-lookup"><span data-stu-id="2dc36-125">Select the reason</span></span>
10. <span data-ttu-id="2dc36-126">在详细信息字段中，输入更具描述性的申请理由</span><span class="sxs-lookup"><span data-stu-id="2dc36-126">In the details field enter a more descriptive justification for the requisition</span></span>

## <a name="add-a-line-to-the-requisition"></a><span data-ttu-id="2dc36-127">添加行到申请。</span><span class="sxs-lookup"><span data-stu-id="2dc36-127">Add a line to the requisition</span></span>
1. <span data-ttu-id="2dc36-128">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="2dc36-128">Click Add line.</span></span>
    * <span data-ttu-id="2dc36-129">有两种方式可以将行添加到采购申请中。</span><span class="sxs-lookup"><span data-stu-id="2dc36-129">There are two ways of adding lines to the purchase requisition.</span></span> <span data-ttu-id="2dc36-130">如果您已经知道产品编号或已经知道您申请的产品不在产品目录中，则您可以直接使用“添加行”来添加行。</span><span class="sxs-lookup"><span data-stu-id="2dc36-130">If you already know the product number or you already  know that you are requesting a product that is not in the product catalog, then you can add the line directly with "Add line".</span></span> <span data-ttu-id="2dc36-131">另一种方法是使用“添加产品”，在此处您可以使用搜索和筛选查找产品目录中的物料。</span><span class="sxs-lookup"><span data-stu-id="2dc36-131">The other way is to use "Add products" where you can use searching and filtering to find items in the product catalog.</span></span>    
2. <span data-ttu-id="2dc36-132">单击您刚创建的行。</span><span class="sxs-lookup"><span data-stu-id="2dc36-132">Click on the row you just created.</span></span>
    * <span data-ttu-id="2dc36-133">申请者是已提交申请的工作人员。</span><span class="sxs-lookup"><span data-stu-id="2dc36-133">The requester is the worker that has requested the requisition.</span></span>   
    * <span data-ttu-id="2dc36-134">默认情况下，准备申请的人员是已提交申请的工作人员。</span><span class="sxs-lookup"><span data-stu-id="2dc36-134">By default the person preparing the requisition is the worker who has requested it.</span></span> <span data-ttu-id="2dc36-135">您必须获得权限，以代表其他工作人员准备申请行。</span><span class="sxs-lookup"><span data-stu-id="2dc36-135">You have to be given permission to prepare a requisition line on behalf of another worker.</span></span> <span data-ttu-id="2dc36-136">如果您拥有此类权限，则其他工作人员将会在本查找中显示。</span><span class="sxs-lookup"><span data-stu-id="2dc36-136">If you have such permissions then the other workers will show up in this lookup.</span></span>  
3. <span data-ttu-id="2dc36-137">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="2dc36-137">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="2dc36-138">可供您选择的物料受到采购法人实体的类别访问策略和采购目录的限制。</span><span class="sxs-lookup"><span data-stu-id="2dc36-138">The items that are available for you to choose are limited by the category access policy and the procurement catalog for the buying legal entity.</span></span>   
4. <span data-ttu-id="2dc36-139">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="2dc36-139">In the Quantity field, enter a number.</span></span>

## <a name="add-more-products-to-the-requisition"></a><span data-ttu-id="2dc36-140">添加更多产品到申请</span><span class="sxs-lookup"><span data-stu-id="2dc36-140">Add more products to the requisition</span></span>
1. <span data-ttu-id="2dc36-141">单击 添加产品。</span><span class="sxs-lookup"><span data-stu-id="2dc36-141">Click Add products.</span></span>
    * <span data-ttu-id="2dc36-142">此选项可供您在其中检索产品目录中的产品。</span><span class="sxs-lookup"><span data-stu-id="2dc36-142">This is the option where you can search for products in the product catalog.</span></span>    
2. <span data-ttu-id="2dc36-143">在“查找采购类别节点”字段中，键入您正在查找的类别的名称的第一部分，然后单击 "Enter" 键。</span><span class="sxs-lookup"><span data-stu-id="2dc36-143">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="2dc36-144">例如，键入计算。</span><span class="sxs-lookup"><span data-stu-id="2dc36-144">For example, type comput.</span></span>  
3. <span data-ttu-id="2dc36-145">使用“InvokeDefaultButton”快捷方式。</span><span class="sxs-lookup"><span data-stu-id="2dc36-145">Use the InvokeDefaultButton shortcut.</span></span>
4. <span data-ttu-id="2dc36-146">使用“筛选器”筛选选定类别中的产品列表。</span><span class="sxs-lookup"><span data-stu-id="2dc36-146">Use the Filter to filter the list of products in the selected category.</span></span>
5. <span data-ttu-id="2dc36-147">选择您想要添加到申请的产品卡。</span><span class="sxs-lookup"><span data-stu-id="2dc36-147">Select the product card that you want to add to the requisition.</span></span>
6. <span data-ttu-id="2dc36-148">单击“添加到行”。</span><span class="sxs-lookup"><span data-stu-id="2dc36-148">Click Add to lines.</span></span>
7. <span data-ttu-id="2dc36-149">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="2dc36-149">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="2dc36-150">在“查找采购类别节点”字段中，键入您正在查找的类别的名称的第一部分，然后单击 "Enter" 键。</span><span class="sxs-lookup"><span data-stu-id="2dc36-150">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="2dc36-151">例如，键入高（萤光笔）。</span><span class="sxs-lookup"><span data-stu-id="2dc36-151">For example, type High (highlighters).</span></span>  
9. <span data-ttu-id="2dc36-152">使用“InvokeDefaultButton”快捷方式。</span><span class="sxs-lookup"><span data-stu-id="2dc36-152">Use the InvokeDefaultButton shortcut.</span></span>
10. <span data-ttu-id="2dc36-153">单击“添加未列示产品到行”以添加到未列示在采购目录中的产品。</span><span class="sxs-lookup"><span data-stu-id="2dc36-153">Click Add unlisted product to lines to add a product that’s not listed in the procurement catalog.</span></span>
11. <span data-ttu-id="2dc36-154">在“产品名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="2dc36-154">In the Product name field, type a value.</span></span>
12. <span data-ttu-id="2dc36-155">在“单位”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="2dc36-155">In the Unit field, type a value.</span></span>
13. <span data-ttu-id="2dc36-156">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2dc36-156">Click OK.</span></span>
14. <span data-ttu-id="2dc36-157">在“物料说明”字段中，添加产品说明。</span><span class="sxs-lookup"><span data-stu-id="2dc36-157">In the Item description field, add a description of the product.</span></span>
15. <span data-ttu-id="2dc36-158">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="2dc36-158">In the Quantity field, enter a number.</span></span>
16. <span data-ttu-id="2dc36-159">在“单位价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="2dc36-159">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="2dc36-160">如果您知道特定供应商的价格（您在供应商帐户字段中选择的），则可以输入该价格</span><span class="sxs-lookup"><span data-stu-id="2dc36-160">If you know the price for a particular vendor (that you select in the vendor account field) then that price can be entered</span></span>   
17. <span data-ttu-id="2dc36-161">在“供应商帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="2dc36-161">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2dc36-162">可用在此字段使用的供应商取决于采购政策和供应商当前采购类别的状态。</span><span class="sxs-lookup"><span data-stu-id="2dc36-162">The vendors that are available in this field depend on the purchasing policies and the status that the vendor has for the current procurement category.</span></span> <span data-ttu-id="2dc36-163">除了在此处选择供应商的备选方法，可以单击“建议供应商”按钮。</span><span class="sxs-lookup"><span data-stu-id="2dc36-163">As an alternative to selecting a vendor here, you can click the Suggest vendor button.</span></span>    
18. <span data-ttu-id="2dc36-164">在列表中，选择您想要使用的供应商。</span><span class="sxs-lookup"><span data-stu-id="2dc36-164">In the list, select the vendor you want to use.</span></span>
19. <span data-ttu-id="2dc36-165">在“外部物料编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="2dc36-165">In the External item number field, type a value.</span></span>
    * <span data-ttu-id="2dc36-166">这是供应商已知的产品的参考编号。</span><span class="sxs-lookup"><span data-stu-id="2dc36-166">This is a reference number for the product that is known by the vendor.</span></span> <span data-ttu-id="2dc36-167">例如，这可能是供应商自己的产品目录中的产品的物料编号。</span><span class="sxs-lookup"><span data-stu-id="2dc36-167">For example, this could be the item number of the product in the vendor's own catalog.</span></span>  
20. <span data-ttu-id="2dc36-168">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2dc36-168">Click OK.</span></span>

## <a name="distribute-amounts"></a><span data-ttu-id="2dc36-169">分摊金额</span><span class="sxs-lookup"><span data-stu-id="2dc36-169">Distribute amounts</span></span>
1. <span data-ttu-id="2dc36-170">单击“财务”。</span><span class="sxs-lookup"><span data-stu-id="2dc36-170">Click Financials.</span></span>
2. <span data-ttu-id="2dc36-171">单击“分配金额”。</span><span class="sxs-lookup"><span data-stu-id="2dc36-171">Click Distribute amounts.</span></span>
    * <span data-ttu-id="2dc36-172">该过程会显示如何在 2 个帐户之间分配第一行的成本。</span><span class="sxs-lookup"><span data-stu-id="2dc36-172">This process shows you how to distribute the cost for the first line between 2 accounts.</span></span> <span data-ttu-id="2dc36-173">在申请接受审查时，这也可能稍后执行。</span><span class="sxs-lookup"><span data-stu-id="2dc36-173">This can also be done later when the requisition is in review.</span></span>  
3. <span data-ttu-id="2dc36-174">单击“拆分”以新建分配行。</span><span class="sxs-lookup"><span data-stu-id="2dc36-174">Click Split to create a new distribution line.</span></span>
4. <span data-ttu-id="2dc36-175">在“分类帐户”字段中，选择第一个应负担成本的成本中心。</span><span class="sxs-lookup"><span data-stu-id="2dc36-175">In the Ledger account field select the first cost center that should take part of the cost.</span></span>
5. <span data-ttu-id="2dc36-176">选择其他分配行。</span><span class="sxs-lookup"><span data-stu-id="2dc36-176">Select the other distribution line.</span></span>
6. <span data-ttu-id="2dc36-177">在“分类帐户”字段中，指定其他成本中心。</span><span class="sxs-lookup"><span data-stu-id="2dc36-177">In the Ledger account field specify the other cost center.</span></span>
7. <span data-ttu-id="2dc36-178">单击“平均分配”。</span><span class="sxs-lookup"><span data-stu-id="2dc36-178">Click Distribute equally.</span></span>
8. <span data-ttu-id="2dc36-179">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2dc36-179">Close the page.</span></span>

## <a name="view-line-details"></a><span data-ttu-id="2dc36-180">查看行明细</span><span class="sxs-lookup"><span data-stu-id="2dc36-180">View line details</span></span>
1. <span data-ttu-id="2dc36-181">切换“行详细信息”部分的扩展。</span><span class="sxs-lookup"><span data-stu-id="2dc36-181">Toggle the expansion of the Line details section.</span></span>

## <a name="submit-the-requisition"></a><span data-ttu-id="2dc36-182">提交申请</span><span class="sxs-lookup"><span data-stu-id="2dc36-182">Submit the requisition</span></span>
1. <span data-ttu-id="2dc36-183">单击“工作流程”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="2dc36-183">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="2dc36-184">单击“提交”。</span><span class="sxs-lookup"><span data-stu-id="2dc36-184">Click Submit.</span></span>
3. <span data-ttu-id="2dc36-185">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2dc36-185">Close the page.</span></span>
4. <span data-ttu-id="2dc36-186">在“注解”字段中，键入申请批准人的附注。</span><span class="sxs-lookup"><span data-stu-id="2dc36-186">In the Comment field, type a note for the approver of the requisition.</span></span>
5. <span data-ttu-id="2dc36-187">单击“提交”。</span><span class="sxs-lookup"><span data-stu-id="2dc36-187">Click Submit.</span></span>
6. <span data-ttu-id="2dc36-188">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2dc36-188">Close the page.</span></span>
7. <span data-ttu-id="2dc36-189">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="2dc36-189">Refresh the page.</span></span>


