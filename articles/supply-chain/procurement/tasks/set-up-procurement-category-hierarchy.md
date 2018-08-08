--- 
title: "设置采购类别层次结构"
description: "该过程会显示如何在采购类别层次结构中创建新节点，以及如何配置采购类别以用于采购流程。"
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 01809a8a3256342682d8a9cfb296a355310fe4ed
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="d3f07-103">设置采购类别层次结构</span><span class="sxs-lookup"><span data-stu-id="d3f07-103">Set up a procurement category hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d3f07-104">该过程会显示如何在采购类别层次结构中创建新节点，以及如何配置采购类别以用于采购流程。</span><span class="sxs-lookup"><span data-stu-id="d3f07-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="d3f07-105">这些任务通常由采购经理完成。</span><span class="sxs-lookup"><span data-stu-id="d3f07-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="d3f07-106">在您开始该过程之前，采购类型层次结构必须存在。</span><span class="sxs-lookup"><span data-stu-id="d3f07-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="d3f07-107">如果您正在使用公司演示数据，则您可以在 USMF 公司中执行该过程。</span><span class="sxs-lookup"><span data-stu-id="d3f07-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="d3f07-108">添加新采购类别</span><span class="sxs-lookup"><span data-stu-id="d3f07-108">Add a new procurement category</span></span>
1. <span data-ttu-id="d3f07-109">转到采购>采购目录。 </span><span class="sxs-lookup"><span data-stu-id="d3f07-109">Go to Procurement and sourcing > Procurement categories.</span></span>
2. <span data-ttu-id="d3f07-110">单击“编辑类别层次结构”。</span><span class="sxs-lookup"><span data-stu-id="d3f07-110">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="d3f07-111">当前采购类别层次结构会显示在页左侧。</span><span class="sxs-lookup"><span data-stu-id="d3f07-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="d3f07-112">您即将修改该层次结构。</span><span class="sxs-lookup"><span data-stu-id="d3f07-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="d3f07-113">单击“新类别节点”。</span><span class="sxs-lookup"><span data-stu-id="d3f07-113">Click New category node.</span></span>
    * <span data-ttu-id="d3f07-114">系统会默认选择顶端节点。</span><span class="sxs-lookup"><span data-stu-id="d3f07-114">The system selects the top node by default.</span></span> <span data-ttu-id="d3f07-115">如果您正在运行该过程以作为任务指南，您可以单击“解除锁定”按钮，并选择另一个父节点，以插入您的新节点。</span><span class="sxs-lookup"><span data-stu-id="d3f07-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="d3f07-116">一旦完成此项操作，再次锁定任务指南，然后单击“新类别节点”。</span><span class="sxs-lookup"><span data-stu-id="d3f07-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="d3f07-117">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d3f07-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d3f07-118">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d3f07-118">In the Description field, type a value.</span></span>
6. <span data-ttu-id="d3f07-119">在“易记名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d3f07-119">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="d3f07-120">易记名称是可选的。</span><span class="sxs-lookup"><span data-stu-id="d3f07-120">The friendly name is optional.</span></span> <span data-ttu-id="d3f07-121">它将连同类别名称一起显示在类别查找中。</span><span class="sxs-lookup"><span data-stu-id="d3f07-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="d3f07-122">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d3f07-122">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="d3f07-123">添加产品到您的新采购类别</span><span class="sxs-lookup"><span data-stu-id="d3f07-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="d3f07-124">转到采购>采购目录。 </span><span class="sxs-lookup"><span data-stu-id="d3f07-124">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="d3f07-125">选择您刚添加的节点。</span><span class="sxs-lookup"><span data-stu-id="d3f07-125">Select the node you just added.</span></span> <span data-ttu-id="d3f07-126">如果您正在运行该过程以作为任务指南，您可能需要解除任务指南锁定，以选择节点。</span><span class="sxs-lookup"><span data-stu-id="d3f07-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="d3f07-127">切换“产品”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="d3f07-127">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="d3f07-128">单击“添加”以关联产品和采购类别。</span><span class="sxs-lookup"><span data-stu-id="d3f07-128">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="d3f07-129">选择您想要添加到采购类别的产品。</span><span class="sxs-lookup"><span data-stu-id="d3f07-129">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="d3f07-130">单击箭头以选择产品。</span><span class="sxs-lookup"><span data-stu-id="d3f07-130">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="d3f07-131">选择要添加到采购类别的另一个产品。</span><span class="sxs-lookup"><span data-stu-id="d3f07-131">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="d3f07-132">单击箭头以选择产品。</span><span class="sxs-lookup"><span data-stu-id="d3f07-132">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="d3f07-133">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d3f07-133">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="d3f07-134">添加核准供应商和首选供应商</span><span class="sxs-lookup"><span data-stu-id="d3f07-134">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="d3f07-135">切换供应商部分的扩展。</span><span class="sxs-lookup"><span data-stu-id="d3f07-135">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="d3f07-136">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d3f07-136">Click Add.</span></span>
    * <span data-ttu-id="d3f07-137">您可以添加一个供应商到采购类别，并指定供应商是否为该类别的首选供应商或只是核准供应商。</span><span class="sxs-lookup"><span data-stu-id="d3f07-137">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="d3f07-138">在您从某一类别中删除某一供应商时，类别中该供应商的历史交易记录不会被删除。</span><span class="sxs-lookup"><span data-stu-id="d3f07-138">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="d3f07-139">查找您想要添加到该采购类别的供应商。</span><span class="sxs-lookup"><span data-stu-id="d3f07-139">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="d3f07-140">单击箭头以选择供应商。</span><span class="sxs-lookup"><span data-stu-id="d3f07-140">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="d3f07-141">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d3f07-141">Click OK.</span></span>
6. <span data-ttu-id="d3f07-142">选择您想要修改的供应商行。</span><span class="sxs-lookup"><span data-stu-id="d3f07-142">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="d3f07-143">在“供应商状态”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d3f07-143">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="d3f07-144">类别策略规则中的供应商选择设置会管制采购申请上的所有供应商是否为首选、核准或可用供应商。</span><span class="sxs-lookup"><span data-stu-id="d3f07-144">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="d3f07-145">添加附加信息到该类别</span><span class="sxs-lookup"><span data-stu-id="d3f07-145">Add additional information to the category</span></span>
1. <span data-ttu-id="d3f07-146">切换“供应商评估条件组”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="d3f07-146">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="d3f07-147">此选项卡可使您定义该采购类别中的供应商应根据什么标准进行评级。</span><span class="sxs-lookup"><span data-stu-id="d3f07-147">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="d3f07-148">为此，您可以单击“添加”，然后选择一个包含您想要条件的供应商评估组。</span><span class="sxs-lookup"><span data-stu-id="d3f07-148">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="d3f07-149">切换“调查问卷”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="d3f07-149">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="d3f07-150">此选项卡可使您添加将在申请中显示的调查问卷，只要您将“活动类型”设置为“申请”。</span><span class="sxs-lookup"><span data-stu-id="d3f07-150">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="d3f07-151">然后，申请者必须填写调查问卷，从而才能提交关于该采购类别中特定产品的申请。</span><span class="sxs-lookup"><span data-stu-id="d3f07-151">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="d3f07-152">切换物料销售税组部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="d3f07-152">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="d3f07-153">在“物料销售税组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="d3f07-153">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d3f07-154">选择增值税组。</span><span class="sxs-lookup"><span data-stu-id="d3f07-154">Select a sales tax group.</span></span>
6. <span data-ttu-id="d3f07-155">切换“类别页”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="d3f07-155">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="d3f07-156">可在类别层次结构页中创建类别页。</span><span class="sxs-lookup"><span data-stu-id="d3f07-156">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="d3f07-157">它们包含关于采购类别的信息（例如关于类别中的产品类型信息）、类别中的产品图形或通告（例如类别中可用的折扣）。</span><span class="sxs-lookup"><span data-stu-id="d3f07-157">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="d3f07-158">某个类别页中的信息会显示在采购申请上。</span><span class="sxs-lookup"><span data-stu-id="d3f07-158">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="d3f07-159">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d3f07-159">Close the page.</span></span>


