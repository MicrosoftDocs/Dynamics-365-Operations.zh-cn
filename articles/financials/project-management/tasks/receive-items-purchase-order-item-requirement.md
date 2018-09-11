--- 
title: "根据物料需求接收采购订单上的物料"
description: "此过程显示如何根据物料需求接收某一采购订单的物料。"
author: KimANelson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: faaea6c46e83dc85e9b7efe7a9ca5c261811a3de
ms.contentlocale: zh-cn
ms.lasthandoff: 09/11/2018

---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="4f6d7-103">根据物料需求接收采购订单上的物料</span><span class="sxs-lookup"><span data-stu-id="4f6d7-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4f6d7-104">此过程显示如何根据物料需求接收某一采购订单的物料。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="4f6d7-105">通过使用物料需求来代替物料交易记录，您可以计划刚好在实际使用物料之前交货，创建采购订单，在贸易协议框架中包括物料，以及在生产计划中包括物料需求。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="4f6d7-106">此任务使用 USSI 数据集。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="4f6d7-107">转到项目管理和记账>项目>全部项目。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="4f6d7-108">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="4f6d7-109">在操作窗格上，单击“计划”。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="4f6d7-110">单击“物料需求”。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-110">Click Item requirements.</span></span>
5. <span data-ttu-id="4f6d7-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-111">Click New.</span></span>
6. <span data-ttu-id="4f6d7-112">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="4f6d7-113">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="4f6d7-114">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="4f6d7-115">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-115">Click Save.</span></span>
10. <span data-ttu-id="4f6d7-116">在“操作窗格”上单击“管理”。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="4f6d7-117">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-117">Click Functions.</span></span>
12. <span data-ttu-id="4f6d7-118">单击“创建采购订单”。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="4f6d7-119">选中“包括”复选框。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-119">Select the Include check box.</span></span>
14. <span data-ttu-id="4f6d7-120">在“供应商帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="4f6d7-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-121">Click OK.</span></span>
16. <span data-ttu-id="4f6d7-122">转到“应付账款”>“采购订单”>“所有采购订单”。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="4f6d7-123">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="4f6d7-124">在操作窗格上，单击“采购”。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="4f6d7-125">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-125">Click Confirm.</span></span>
20. <span data-ttu-id="4f6d7-126">在操作窗格上，单击“接收”。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="4f6d7-127">单击“产品收据”。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-127">Click Product receipt.</span></span>
22. <span data-ttu-id="4f6d7-128">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="4f6d7-129">在“产品收据”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="4f6d7-130">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4f6d7-130">Click OK.</span></span>


