---
title: 创建采购协议
description: 该过程会从头至尾指导您创建一份采购协议。
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: df74eaad51fc4ef28caf96e4bcdc7b03f7e6ec3b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836344"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="8a830-103">创建采购协议</span><span class="sxs-lookup"><span data-stu-id="8a830-103">Create a purchase agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8a830-104">该过程会从头至尾指导您创建一份采购协议。</span><span class="sxs-lookup"><span data-stu-id="8a830-104">This procedure guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="8a830-105">这通常由采购经理完成。</span><span class="sxs-lookup"><span data-stu-id="8a830-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="8a830-106">您可以使用演示数据公司 USMF，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="8a830-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="8a830-107">在您开始之前，您需要设置采购协议分类。</span><span class="sxs-lookup"><span data-stu-id="8a830-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="8a830-108">一旦创建完协议，您可以在创建采购订单时使用该协议，并且这会将采购协议条件复制到受该协议影响的订单的标题和任何行。</span><span class="sxs-lookup"><span data-stu-id="8a830-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="8a830-109">新建采购协议</span><span class="sxs-lookup"><span data-stu-id="8a830-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="8a830-110">转到“采购”>“采购协议”>“采购协议”。</span><span class="sxs-lookup"><span data-stu-id="8a830-110">Go to Procurement and sourcing > Purchase agreements > Purchase agreements.</span></span>
2. <span data-ttu-id="8a830-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8a830-111">Click New.</span></span>
3. <span data-ttu-id="8a830-112">在“供应商帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="8a830-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8a830-113">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="8a830-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="8a830-114">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="8a830-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8a830-115">在“采购协议分类”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="8a830-115">In the Purchase agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8a830-116">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="8a830-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="8a830-117">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="8a830-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8a830-118">展开“常规”部分。</span><span class="sxs-lookup"><span data-stu-id="8a830-118">Expand the General section.</span></span>
10. <span data-ttu-id="8a830-119">在“到期日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="8a830-119">In the Expiration date field, enter a date.</span></span>
    * <span data-ttu-id="8a830-120">此到期日期将是所有承诺行的默认设置，并将确定每个特定承诺的有效期有多长。</span><span class="sxs-lookup"><span data-stu-id="8a830-120">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  
11. <span data-ttu-id="8a830-121">在“文件标题”字段中，键入您的采购协议的名称。</span><span class="sxs-lookup"><span data-stu-id="8a830-121">In the Document title field, type a name for your purchase agreement.</span></span>
    * <span data-ttu-id="8a830-122">将“默认承诺”字段设置为“产品数量承诺”（或者进行更改，如果未设置为产品数量承诺）。</span><span class="sxs-lookup"><span data-stu-id="8a830-122">Leave the Default commitment field set to Product quantity commitment (or change it if it’s not set to this).</span></span>  
    * <span data-ttu-id="8a830-123">默认承诺值可确定您在协议行上的选项。</span><span class="sxs-lookup"><span data-stu-id="8a830-123">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="8a830-124">如果在创建协议行时，您需要新的承诺类型，则您需要更改标题上的默认承诺。</span><span class="sxs-lookup"><span data-stu-id="8a830-124">If you need a new commitment type when you’re creating the agreement lines, you need to change the default commitment on the header.</span></span>  <span data-ttu-id="8a830-125">共有 4 种类型的承诺：产品数量承诺 - 适用于特定数量的产品；产品价值承诺 - 适用于特定币种金额的产品；产品类别价值承诺 - 适用于特定币种金额的采购类别，其中金额可以是某一目录物料或非目录物料的金额；价值承诺 - 适用于可由任何产品或任何采购类别实现的特定币种金额。</span><span class="sxs-lookup"><span data-stu-id="8a830-125">There are 4 types of commitments: Product quantity commitment - for a specific quantity of a product; Product value commitment - for a specific currency amount of a product; Product category value commitment - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; Value commitment - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  
12. <span data-ttu-id="8a830-126">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8a830-126">Click OK.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="8a830-127">添加承诺</span><span class="sxs-lookup"><span data-stu-id="8a830-127">Add a commitment</span></span>
1. <span data-ttu-id="8a830-128">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="8a830-128">Click Add line.</span></span>
2. <span data-ttu-id="8a830-129">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="8a830-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="8a830-130">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="8a830-130">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8a830-131">选择您想为其添加承诺的产品。</span><span class="sxs-lookup"><span data-stu-id="8a830-131">Select the product you want to add a commitment for.</span></span>
5. <span data-ttu-id="8a830-132">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="8a830-132">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8a830-133">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="8a830-133">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8a830-134">这是您同意从供应商采购的总数量。</span><span class="sxs-lookup"><span data-stu-id="8a830-134">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
7. <span data-ttu-id="8a830-135">在“单位价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="8a830-135">In the Unit price field, enter a number.</span></span>
8. <span data-ttu-id="8a830-136">展开“行明细”部分。</span><span class="sxs-lookup"><span data-stu-id="8a830-136">Expand the Line details section.</span></span>
9. <span data-ttu-id="8a830-137">将“最大值”强制选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="8a830-137">Set the Max is enforced option to Yes.</span></span>
    * <span data-ttu-id="8a830-138">“最大值”是强制执行的选项，以限制承诺的使用。</span><span class="sxs-lookup"><span data-stu-id="8a830-138">The Max is enforced option limits the use of the commitment.</span></span> <span data-ttu-id="8a830-139">您只能最多购买“数量”字段中规定的该行的数量。</span><span class="sxs-lookup"><span data-stu-id="8a830-139">You can only purchase up to the quantity that's specified in the Quantity field for the line.</span></span>  
10. <span data-ttu-id="8a830-140">收起“行详情”部分。</span><span class="sxs-lookup"><span data-stu-id="8a830-140">Collapse the Line details section.</span></span>

## <a name="add-header-conditions"></a><span data-ttu-id="8a830-141">添加标题条件</span><span class="sxs-lookup"><span data-stu-id="8a830-141">Add header conditions</span></span>
1. <span data-ttu-id="8a830-142">在“操作窗格”上，单击“选项”。</span><span class="sxs-lookup"><span data-stu-id="8a830-142">On the Action Pane, click Options.</span></span>
2. <span data-ttu-id="8a830-143">单击“更改”视图。</span><span class="sxs-lookup"><span data-stu-id="8a830-143">Click Change view.</span></span>
3. <span data-ttu-id="8a830-144">单击“标题”视图。</span><span class="sxs-lookup"><span data-stu-id="8a830-144">Click Header view.</span></span>
4. <span data-ttu-id="8a830-145">展开“条款”部分。</span><span class="sxs-lookup"><span data-stu-id="8a830-145">Expand the Terms section.</span></span>
5. <span data-ttu-id="8a830-146">在“付款方式”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="8a830-146">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8a830-147">供应商帐户的付款条件会默认显示在此。</span><span class="sxs-lookup"><span data-stu-id="8a830-147">The payment terms from the vendor account are shown here by default.</span></span>       
6. <span data-ttu-id="8a830-148">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="8a830-148">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="8a830-149">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="8a830-149">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="8a830-150">在“交货方式”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="8a830-150">In the Mode of delivery field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="8a830-151">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="8a830-151">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="8a830-152">在“交货条款”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="8a830-152">In the Delivery terms field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="8a830-153">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="8a830-153">In the list, click the link in the selected row.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="8a830-154">确认并激活协议</span><span class="sxs-lookup"><span data-stu-id="8a830-154">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="8a830-155">在“操作窗格”上单击“采购协议”。</span><span class="sxs-lookup"><span data-stu-id="8a830-155">On the Action Pane, click Purchase agreement.</span></span>
2. <span data-ttu-id="8a830-156">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="8a830-156">Click Confirmation.</span></span>
    * <span data-ttu-id="8a830-157">将“标记协议为有效选项”设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="8a830-157">Set the Mark agreement as effective option to Yes.</span></span>  
3. <span data-ttu-id="8a830-158">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8a830-158">Click OK.</span></span>
4. <span data-ttu-id="8a830-159">在“操作窗格”上单击“采购协议”。</span><span class="sxs-lookup"><span data-stu-id="8a830-159">On the Action Pane, click Purchase agreement.</span></span>
5. <span data-ttu-id="8a830-160">单击“采购协议确认”。</span><span class="sxs-lookup"><span data-stu-id="8a830-160">Click Purchase agreement confirmations.</span></span>
    * <span data-ttu-id="8a830-161">“预览/打印”选项允许您生成一份采购协议文件，然后您可以打印或发送给供应商。</span><span class="sxs-lookup"><span data-stu-id="8a830-161">The Preview/Print option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="8a830-162">如果您随后更新并再次确认该协议，则会在此显示两个版本的协议。</span><span class="sxs-lookup"><span data-stu-id="8a830-162">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="8a830-163">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8a830-163">Close the page.</span></span>

