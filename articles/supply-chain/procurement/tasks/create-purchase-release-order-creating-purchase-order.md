---
title: 创建采购订单时创建采购下达单
description: 该过程会显示在创建采购订单时，如何使用采购协议。
author: RichardLuan
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eaa441318ed7d00ce205f4f59b983b25cf97f086
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211974"
---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a><span data-ttu-id="2fa15-103">创建采购订单时创建采购下达单</span><span class="sxs-lookup"><span data-stu-id="2fa15-103">Create a purchase release order when creating the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2fa15-104">该过程会显示在创建采购订单时，如何使用采购协议。</span><span class="sxs-lookup"><span data-stu-id="2fa15-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="2fa15-105">在创建采购订单时必须应用采购协议，因为存在应复制到采购订单标题的一般条件。</span><span class="sxs-lookup"><span data-stu-id="2fa15-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="2fa15-106">此任务通常由采购人员完成。</span><span class="sxs-lookup"><span data-stu-id="2fa15-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="2fa15-107">作为本指南的先决条件，您必须拥有某个供应商和物料的带产品数量承诺的有效采购协议。</span><span class="sxs-lookup"><span data-stu-id="2fa15-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="2fa15-108">如果您拥有带其他类型承诺的采购协议，则可以使用相同过程。</span><span class="sxs-lookup"><span data-stu-id="2fa15-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="2fa15-109">您可以使用 USMF 公司演示数据运行此指南。</span><span class="sxs-lookup"><span data-stu-id="2fa15-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="2fa15-110">如果您正在使用 USMF，您可以先运行“创建采购协议”，以设置本指南所需的前提条件。</span><span class="sxs-lookup"><span data-stu-id="2fa15-110">If you're using USMF, you can run the "Create a purchase agreement" guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="2fa15-111">创建采购订单</span><span class="sxs-lookup"><span data-stu-id="2fa15-111">Create a purchase order</span></span>
1. <span data-ttu-id="2fa15-112">打开采购订单准备工作区。</span><span class="sxs-lookup"><span data-stu-id="2fa15-112">Open the purchase order preparation workspace.</span></span>
2. <span data-ttu-id="2fa15-113">单击“新采购订单”。</span><span class="sxs-lookup"><span data-stu-id="2fa15-113">Click New purchase order.</span></span>
3. <span data-ttu-id="2fa15-114">在“供应商帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="2fa15-114">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2fa15-115">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="2fa15-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="2fa15-116">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="2fa15-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="2fa15-117">切换“概况”部分的扩展。</span><span class="sxs-lookup"><span data-stu-id="2fa15-117">Toggle the expansion of the General section.</span></span>
7. <span data-ttu-id="2fa15-118">在“采购协议”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="2fa15-118">In the Purchase agreement field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2fa15-119">该供应商的所有可用协议皆列示于此。</span><span class="sxs-lookup"><span data-stu-id="2fa15-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="2fa15-120">查找您想要使用的有效协议。</span><span class="sxs-lookup"><span data-stu-id="2fa15-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="2fa15-121">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="2fa15-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="2fa15-122">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="2fa15-122">Click Yes.</span></span>
10. <span data-ttu-id="2fa15-123">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2fa15-123">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="2fa15-124">添加行</span><span class="sxs-lookup"><span data-stu-id="2fa15-124">Add a line</span></span>
1. <span data-ttu-id="2fa15-125">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="2fa15-125">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="2fa15-126">如果承诺的特定库存或位置维度存在，您必须在采购订单行上输入相同的值，以便利用协议。</span><span class="sxs-lookup"><span data-stu-id="2fa15-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="2fa15-127">在“位置”字段中，单击下拉按钮打开查询。</span><span class="sxs-lookup"><span data-stu-id="2fa15-127">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2fa15-128">站点可能已填充来自订单或供应商的默认值。</span><span class="sxs-lookup"><span data-stu-id="2fa15-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="2fa15-129">如果是这种情况，请跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="2fa15-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="2fa15-130">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="2fa15-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="2fa15-131">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="2fa15-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="2fa15-132">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="2fa15-132">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="2fa15-133">验证价格是从承诺复制而来的。</span><span class="sxs-lookup"><span data-stu-id="2fa15-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="2fa15-134">查找承诺</span><span class="sxs-lookup"><span data-stu-id="2fa15-134">Look up the commitment</span></span>
1. <span data-ttu-id="2fa15-135">单击“更新行”。</span><span class="sxs-lookup"><span data-stu-id="2fa15-135">Click Update line.</span></span>
2. <span data-ttu-id="2fa15-136">单击“已附加”。</span><span class="sxs-lookup"><span data-stu-id="2fa15-136">Click Attached.</span></span>
    * <span data-ttu-id="2fa15-137">您可在此获得采购协议的详情。</span><span class="sxs-lookup"><span data-stu-id="2fa15-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="2fa15-138">例如，您可以查看价格以及价格和折扣是否被固定，这意味着，如果您将采购订单上的价格或折扣更改为不同于承诺载明的值，系统将会删除链接，以使采购订单行不履行承诺。</span><span class="sxs-lookup"><span data-stu-id="2fa15-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="2fa15-139">您还可以查看是否选择“最大值”是强制执行的选项，这意味着所有履行承诺的订单的数量综合不能超过承诺载明的数量。</span><span class="sxs-lookup"><span data-stu-id="2fa15-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="2fa15-140">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2fa15-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="2fa15-141">查找采购协议</span><span class="sxs-lookup"><span data-stu-id="2fa15-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="2fa15-142">在操作窗格上，单击“常规”。</span><span class="sxs-lookup"><span data-stu-id="2fa15-142">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="2fa15-143">单击“采购协议”。</span><span class="sxs-lookup"><span data-stu-id="2fa15-143">Click Purchase agreement.</span></span>
3. <span data-ttu-id="2fa15-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2fa15-144">Close the page.</span></span>
4. <span data-ttu-id="2fa15-145">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2fa15-145">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]