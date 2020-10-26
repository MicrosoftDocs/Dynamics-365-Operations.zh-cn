---
title: 管理订单保留
description: 此过程演示如何将销售订单置于暂停状态、如何使用订单保留签出，以及如何删除订单保留。
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9caf6651813f0111b873db1769140d973f1a2e3b
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981961"
---
# <a name="manage-order-holds"></a><span data-ttu-id="9a88c-103">管理订单保留</span><span class="sxs-lookup"><span data-stu-id="9a88c-103">Manage order holds</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9a88c-104">此过程演示如何将销售订单置于暂停状态、如何使用订单保留签出，以及如何删除订单保留。</span><span class="sxs-lookup"><span data-stu-id="9a88c-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="9a88c-105">订单可能出于多种原因被置于暂停状态。</span><span class="sxs-lookup"><span data-stu-id="9a88c-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="9a88c-106">例如，在验证客户地址或付款方式之前，或在经理可以查看客户的信用额度之前，您可以保留订单。</span><span class="sxs-lookup"><span data-stu-id="9a88c-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer's credit limit.</span></span> <span data-ttu-id="9a88c-107">订单出于保留状态时，仓库不能为装运处理该订单。</span><span class="sxs-lookup"><span data-stu-id="9a88c-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="9a88c-108">您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="9a88c-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="9a88c-109">设置订单暂停</span><span class="sxs-lookup"><span data-stu-id="9a88c-109">Set up order holds</span></span>
1. <span data-ttu-id="9a88c-110">转到**导航窗格 > 模块 > 销售和营销 > 设置 > 销售订单 > 订单保留代码**。</span><span class="sxs-lookup"><span data-stu-id="9a88c-110">Go to **Navigation pane > Modules > Sales and marketing > Setup > Sales orders > Order hold codes**.</span></span>
2. <span data-ttu-id="9a88c-111">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9a88c-111">Click **New**.</span></span>
3. <span data-ttu-id="9a88c-112">在**保留代码**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a88c-112">In the **Hold code** field, type a value.</span></span> <span data-ttu-id="9a88c-113">例如，输入“回电”。</span><span class="sxs-lookup"><span data-stu-id="9a88c-113">For example, type 'Call back'.</span></span>  
4. <span data-ttu-id="9a88c-114">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a88c-114">In the **Description** field, type a value.</span></span>
    - <span data-ttu-id="9a88c-115">例如，已保留并在等待客户回电的订单。</span><span class="sxs-lookup"><span data-stu-id="9a88c-115">For example, Order held waiting for customer callback.</span></span>  
    - <span data-ttu-id="9a88c-116">或者，也可以选中**删除预留**复选框，以便在添加此保留代码时从订单中删除所有实际预留。</span><span class="sxs-lookup"><span data-stu-id="9a88c-116">Optionally, select the **Remove reservations** check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="9a88c-117">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="9a88c-117">Click **Save**.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="9a88c-118">将订单设置为保留状态</span><span class="sxs-lookup"><span data-stu-id="9a88c-118">Place order on hold</span></span>
1. <span data-ttu-id="9a88c-119">转到**导航窗格 > 模块 > 销售和营销 > 销售订单 > 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="9a88c-119">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="9a88c-120">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9a88c-120">Click **New**.</span></span>
3. <span data-ttu-id="9a88c-121">在**客户帐户**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="9a88c-121">In the **Customer account** field, enter or select a value.</span></span>
4. <span data-ttu-id="9a88c-122">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="9a88c-122">Click **OK**.</span></span>
5. <span data-ttu-id="9a88c-123">在**物料编号**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="9a88c-123">In the **Item number** field, enter or select a value.</span></span>
6. <span data-ttu-id="9a88c-124">在**数量**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9a88c-124">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="9a88c-125">在**操作窗格**上，单击**销售订单**。</span><span class="sxs-lookup"><span data-stu-id="9a88c-125">On the **Action Pane**, click **Sales order**.</span></span>
8. <span data-ttu-id="9a88c-126">单击**订单保留**。</span><span class="sxs-lookup"><span data-stu-id="9a88c-126">Click **Order holds**.</span></span>
9. <span data-ttu-id="9a88c-127">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9a88c-127">Click **New**.</span></span>
10. <span data-ttu-id="9a88c-128">在**保留代码**字段中，选择在上一个子任务中已创建的代码。</span><span class="sxs-lookup"><span data-stu-id="9a88c-128">In the **Hold code** field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="9a88c-129">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="9a88c-129">Click **Save**.</span></span>
12. <span data-ttu-id="9a88c-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9a88c-130">Close the page.</span></span>
13. <span data-ttu-id="9a88c-131">转到**销售和营销 > 销售订单 > 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="9a88c-131">Go to **Sales and marketing > Sales orders > All sales orders**.</span></span>
14. <span data-ttu-id="9a88c-132">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="9a88c-132">In the list, mark the selected row.</span></span> <span data-ttu-id="9a88c-133">当前处于保留状态的订单的“请勿处理”和“保留”字段带有标记。</span><span class="sxs-lookup"><span data-stu-id="9a88c-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>
15. <span data-ttu-id="9a88c-134">在“操作窗格”中，单击**领料和装箱**。</span><span class="sxs-lookup"><span data-stu-id="9a88c-134">On the Action Pane, click **Pick and pack**.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="9a88c-135">管理订单保留</span><span class="sxs-lookup"><span data-stu-id="9a88c-135">Manage order holds</span></span>
1. <span data-ttu-id="9a88c-136">转到**销售和市场营销 > 销售订单 > 未结订单 > 订单保留**。</span><span class="sxs-lookup"><span data-stu-id="9a88c-136">Go to **Sales and marketing > Sales orders > Open orders > Order holds**.</span></span> <span data-ttu-id="9a88c-137">工作台形式的**订单保留**页面功能，可在其中获取所有当前保留和已处理保留的概述，以及处理这些保留和关联的销售订单。</span><span class="sxs-lookup"><span data-stu-id="9a88c-137">**Order holds** page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>     
2. <span data-ttu-id="9a88c-138">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="9a88c-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="9a88c-139">在**操作窗格**上，单击**保留签出**。</span><span class="sxs-lookup"><span data-stu-id="9a88c-139">On the **Action Pane**, click **Hold checkout**.</span></span>
4. <span data-ttu-id="9a88c-140">单击**签出**。</span><span class="sxs-lookup"><span data-stu-id="9a88c-140">Click **Check out**.</span></span>
5. <span data-ttu-id="9a88c-141">在列表中，取消标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="9a88c-141">In the list, unmark the selected row.</span></span> <span data-ttu-id="9a88c-142">**签出目标**字段现在显示您的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="9a88c-142">The **Checkout out to** field now shows your user ID.</span></span>   
6. <span data-ttu-id="9a88c-143">单击**清除签出**。</span><span class="sxs-lookup"><span data-stu-id="9a88c-143">Click **Clear checkout**.</span></span>
7. <span data-ttu-id="9a88c-144">在**操作窗格**上，单击**清除保留**。</span><span class="sxs-lookup"><span data-stu-id="9a88c-144">On the **Action Pane**, click **Clear hold**.</span></span>
    - <span data-ttu-id="9a88c-145">准备好删除保留并允许订单继续到下一个履行步骤时，必须清除保留。</span><span class="sxs-lookup"><span data-stu-id="9a88c-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="9a88c-146">如果不需要更改订单，可以运行“清除保留”操作。</span><span class="sxs-lookup"><span data-stu-id="9a88c-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="9a88c-147">但是，如果在清除保留时必须更新订单，可以使用“清除并修改”操作。</span><span class="sxs-lookup"><span data-stu-id="9a88c-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    - <span data-ttu-id="9a88c-148">仅当您使用呼叫中心功能时，**清除并提交**操作才适用。</span><span class="sxs-lookup"><span data-stu-id="9a88c-148">The **Clear and submit** action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="9a88c-149">单击**清除保留**。</span><span class="sxs-lookup"><span data-stu-id="9a88c-149">Click **Clear holds**.</span></span> <span data-ttu-id="9a88c-150">保留现在已从订单中清除，并且已从“活动保留”列表中删除。</span><span class="sxs-lookup"><span data-stu-id="9a88c-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="9a88c-151">若要根据特定状态查看所有保留及其子集，请更改“显示”字段中的值。</span><span class="sxs-lookup"><span data-stu-id="9a88c-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

