---
title: 创建采购协议
description: 此主题从头至尾指导您创建一份采购协议。
author: kamaybac
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19bfbe7bc78f08dbbc6f9924313749a46672e202
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812318"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="d6672-103">创建采购协议</span><span class="sxs-lookup"><span data-stu-id="d6672-103">Create a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d6672-104">此主题从头至尾指导您创建一份采购协议。</span><span class="sxs-lookup"><span data-stu-id="d6672-104">This topic guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="d6672-105">这通常由采购经理完成。</span><span class="sxs-lookup"><span data-stu-id="d6672-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="d6672-106">您可以使用演示数据公司 USMF，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="d6672-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="d6672-107">在您开始之前，您需要设置采购协议分类。</span><span class="sxs-lookup"><span data-stu-id="d6672-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="d6672-108">一旦创建完协议，您可以在创建采购订单时使用该协议，并且这会将采购协议条件复制到受该协议影响的订单的标题和任何行。</span><span class="sxs-lookup"><span data-stu-id="d6672-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="d6672-109">新建采购协议</span><span class="sxs-lookup"><span data-stu-id="d6672-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="d6672-110">转到 **导航窗格 > 模块 > 采购 > 采购协议 > 采购协议**。</span><span class="sxs-lookup"><span data-stu-id="d6672-110">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase agreements > Purchase agreements**.</span></span>
2. <span data-ttu-id="d6672-111">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="d6672-111">Click **New**.</span></span>
3. <span data-ttu-id="d6672-112">在 **供应商帐户** 字段中，选择下拉菜单，然后选择所需记录的行。</span><span class="sxs-lookup"><span data-stu-id="d6672-112">In the **Vendor account** field, select the drop-down menu and select the row of the desired record.</span></span>
4. <span data-ttu-id="d6672-113">在 **采购协议分类** 字段中，选择下拉菜单，然后选择所需记录的行。</span><span class="sxs-lookup"><span data-stu-id="d6672-113">In the **Purchase agreement classification** field, select the drop-down menu and select the row of the desired record.</span></span>
5. <span data-ttu-id="d6672-114">展开 **常规** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="d6672-114">Expand the **General** FastTab.</span></span>
6. <span data-ttu-id="d6672-115">在 **到期日期** 字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="d6672-115">In the **Expiration date** field, enter a date.</span></span>

    - <span data-ttu-id="d6672-116">此到期日期将是所有承诺行的默认设置，并将确定每个特定承诺的有效期有多长。</span><span class="sxs-lookup"><span data-stu-id="d6672-116">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  

7. <span data-ttu-id="d6672-117">在 **文档标题** 字段中，键入您的采购协议的名称。</span><span class="sxs-lookup"><span data-stu-id="d6672-117">In the **Document title** field, type a name for your purchase agreement.</span></span>

    - <span data-ttu-id="d6672-118">将 **默认承诺** 字段设置为 **产品数量承诺**（或者进行更改，如果未设置为产品数量承诺）。</span><span class="sxs-lookup"><span data-stu-id="d6672-118">Leave the **Default commitment** field set to **Product quantity commitment** (or change it if it's not set to this).</span></span>  
    - <span data-ttu-id="d6672-119">默认承诺值可确定您在协议行上的选项。</span><span class="sxs-lookup"><span data-stu-id="d6672-119">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="d6672-120">如果在创建协议行时，您需要新的承诺类型，则您需要更改标题上的默认承诺。</span><span class="sxs-lookup"><span data-stu-id="d6672-120">If you need a new commitment type when you're creating the agreement lines, you need to change the default commitment on the header.</span></span> <span data-ttu-id="d6672-121">共有 4 种类型的承诺：**产品数量承诺** - 适用于特定数量的产品；**产品价值承诺** - 适用于特定币种金额的产品；**产品类别价值承诺** - 适用于特定币种金额的采购类别，其中金额可以是某一目录物料或非目录物料的金额；**价值承诺** - 适用于可由任何产品或任何采购类别实现的特定币种金额。</span><span class="sxs-lookup"><span data-stu-id="d6672-121">There are 4 types of commitments: **Product quantity commitment** - for a specific quantity of a product; **Product value commitment** - for a specific currency amount of a product; **Product category value commitment** - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; **Value commitment** - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  

8. <span data-ttu-id="d6672-122">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d6672-122">Select **OK**.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="d6672-123">添加承诺</span><span class="sxs-lookup"><span data-stu-id="d6672-123">Add a commitment</span></span>
1. <span data-ttu-id="d6672-124">选择 **添加行**。</span><span class="sxs-lookup"><span data-stu-id="d6672-124">Select **Add line**.</span></span>
2. <span data-ttu-id="d6672-125">在 **物料编号** 字段中，从下拉菜单选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d6672-125">In the **Item number** field, select the desired record from the drop-down menu.</span></span>
3. <span data-ttu-id="d6672-126">在 **数量** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d6672-126">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="d6672-127">这是您同意从供应商采购的总数量。</span><span class="sxs-lookup"><span data-stu-id="d6672-127">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
4. <span data-ttu-id="d6672-128">在 **单价** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d6672-128">In the **Unit price** field, enter a number.</span></span>
5. <span data-ttu-id="d6672-129">展开 **行详细信息** 部分。</span><span class="sxs-lookup"><span data-stu-id="d6672-129">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="d6672-130">将 **强制为最大** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="d6672-130">Set the **Max is enforced** option to **Yes**.</span></span> <span data-ttu-id="d6672-131">**强制为最大** 选项用于限制承诺的使用。</span><span class="sxs-lookup"><span data-stu-id="d6672-131">The **Max is enforced** option limits the use of the commitment.</span></span> <span data-ttu-id="d6672-132">您只能最多购买 **数量** 字段中规定的该行的数量。</span><span class="sxs-lookup"><span data-stu-id="d6672-132">You can only purchase up to the quantity that's specified in the **Quantity** field for the line.</span></span>  

## <a name="add-header-conditions"></a><span data-ttu-id="d6672-133">添加标题条件</span><span class="sxs-lookup"><span data-stu-id="d6672-133">Add header conditions</span></span>
1. <span data-ttu-id="d6672-134">在操作窗格上，选择 **选项**。</span><span class="sxs-lookup"><span data-stu-id="d6672-134">On the Action Pane, select **Options**.</span></span>
2. <span data-ttu-id="d6672-135">选择 **更改视图**。</span><span class="sxs-lookup"><span data-stu-id="d6672-135">Select **Change view**.</span></span>
3. <span data-ttu-id="d6672-136">选择 **标题视图**。</span><span class="sxs-lookup"><span data-stu-id="d6672-136">Select **Header view**.</span></span>
4. <span data-ttu-id="d6672-137">展开 **条款** 部分。</span><span class="sxs-lookup"><span data-stu-id="d6672-137">Expand the **Terms** section.</span></span>
5. <span data-ttu-id="d6672-138">在 **付款方式** 字段中，在下拉菜单中选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d6672-138">In the **Method of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="d6672-139">供应商帐户的付款条件会默认显示在此。</span><span class="sxs-lookup"><span data-stu-id="d6672-139">The payment terms from the vendor account are shown here by default.</span></span>  
6. <span data-ttu-id="d6672-140">在 **交货方式** 字段中，在下拉菜单中选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d6672-140">In the **Mode of delivery** field, select the desired record in the drop-down menu.</span></span>
7. <span data-ttu-id="d6672-141">在 **交货条款** 字段中，选择下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="d6672-141">In the **Delivery terms** field, select the drop-down button to open the lookup.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="d6672-142">确认并激活协议</span><span class="sxs-lookup"><span data-stu-id="d6672-142">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="d6672-143">在操作窗格上单击 **采购协议**。</span><span class="sxs-lookup"><span data-stu-id="d6672-143">On the Action Pane, select **Purchase agreement**.</span></span>
2. <span data-ttu-id="d6672-144">选择 **确认**。</span><span class="sxs-lookup"><span data-stu-id="d6672-144">Select **Confirmation**.</span></span> <span data-ttu-id="d6672-145">将 **标记协议为有效** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="d6672-145">Set the **Mark agreement as effective** option to **Yes**.</span></span>  
3. <span data-ttu-id="d6672-146">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d6672-146">Select **OK**.</span></span>
4. <span data-ttu-id="d6672-147">在操作窗格上单击 **采购协议**。</span><span class="sxs-lookup"><span data-stu-id="d6672-147">On the Action Pane, select **Purchase agreement**.</span></span>
5. <span data-ttu-id="d6672-148">选择 **采购协议确认**。</span><span class="sxs-lookup"><span data-stu-id="d6672-148">Select **Purchase agreement confirmations**.</span></span> <span data-ttu-id="d6672-149">**预览/打印** 选项允许您生成一份采购协议文件，然后您可以打印或发送给供应商。</span><span class="sxs-lookup"><span data-stu-id="d6672-149">The **Preview/Print** option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="d6672-150">如果您随后更新并再次确认该协议，则会在此显示两个版本的协议。</span><span class="sxs-lookup"><span data-stu-id="d6672-150">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="d6672-151">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d6672-151">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]