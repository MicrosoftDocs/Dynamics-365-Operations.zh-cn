--- 
title: "代表他人设置产品订购权限"
description: "此过程演示如何为工作人员授予代表其他工作人员起草采购申请的权限。"
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 35688d191cef06cc15251a6e10a2e8c9afb0e08b
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="5278d-103">代表他人设置产品订购权限</span><span class="sxs-lookup"><span data-stu-id="5278d-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5278d-104">此过程演示如何为工作人员授予代表其他工作人员起草采购申请的权限。</span><span class="sxs-lookup"><span data-stu-id="5278d-104">This procedure shows how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="5278d-105">换句话说，采购申请“准备人”可以为其他“申请人”创建申请。</span><span class="sxs-lookup"><span data-stu-id="5278d-105">In other words, a purchase requisition “preparer” can create a requisition for another “requester.”</span></span> <span data-ttu-id="5278d-106">此过程还演示如何为工作人员授予在不同法人或营运单位中订购物料和服务的权限。</span><span class="sxs-lookup"><span data-stu-id="5278d-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="5278d-107">这些任务通常由采购经理执行。</span><span class="sxs-lookup"><span data-stu-id="5278d-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="5278d-108">您可以在此过程中使用 USMF 演示数据公司的数据，也可以使用您自己的数据。</span><span class="sxs-lookup"><span data-stu-id="5278d-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="5278d-109">授予代表其他工作人员输入采购申请的权限</span><span class="sxs-lookup"><span data-stu-id="5278d-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="5278d-110">转到“采购”>“设置”>“政策”>“采购申请权限”。</span><span class="sxs-lookup"><span data-stu-id="5278d-110">Go to Procurement and sourcing > Setup > Policies > Purchase requisition permissions.</span></span>
    * <span data-ttu-id="5278d-111">确保“当前视图”字段设置为“按准备人”。</span><span class="sxs-lookup"><span data-stu-id="5278d-111">Make sure that the Current view field is set to By preparer.</span></span>  <span data-ttu-id="5278d-112">左窗格中的列表显示已授予为代表其他人起草申请的权限的人员。</span><span class="sxs-lookup"><span data-stu-id="5278d-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="5278d-113">选择要为其授予（准备人）权限的人员。</span><span class="sxs-lookup"><span data-stu-id="5278d-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="5278d-114">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5278d-114">Click Add.</span></span>
4. <span data-ttu-id="5278d-115">找到并选择要添加为申请人的人员。</span><span class="sxs-lookup"><span data-stu-id="5278d-115">Find and select the person to add as a requester.</span></span>
    * <span data-ttu-id="5278d-116">申请人是可被准备人代表创建申请的人员。</span><span class="sxs-lookup"><span data-stu-id="5278d-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    * <span data-ttu-id="5278d-117">如果准备人应该可以代表所选工作人员创建采购申请，请在“授权”字段中选择“特定”。</span><span class="sxs-lookup"><span data-stu-id="5278d-117">In the Authorization field, select Specific if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="5278d-118">如果准备人还需要可以代表向工作人员报告的所有工作人员创建采购申请，请选择“报告”。</span><span class="sxs-lookup"><span data-stu-id="5278d-118">Select Reporting if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="5278d-119">在”生效日期“字段，输入日期。</span><span class="sxs-lookup"><span data-stu-id="5278d-119">In the Effective field, enter a date.</span></span>
6. <span data-ttu-id="5278d-120">在“截止日期”字段，输入日期。</span><span class="sxs-lookup"><span data-stu-id="5278d-120">In the Expiration field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="5278d-121">查看有权为所选工作人员创建采购申请的准备人</span><span class="sxs-lookup"><span data-stu-id="5278d-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="5278d-122">在“当前视图”字段中，选择“按申请人”。</span><span class="sxs-lookup"><span data-stu-id="5278d-122">In the Current view field, select 'By requester'.</span></span>
    * <span data-ttu-id="5278d-123">此视图显示已授予为代表所选工作人员创建采购业务申请权限的准备人列表。</span><span class="sxs-lookup"><span data-stu-id="5278d-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="5278d-124">使用快速筛选器查找您刚才添加为申请人的工作人员。</span><span class="sxs-lookup"><span data-stu-id="5278d-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="5278d-125">选择该申请人。</span><span class="sxs-lookup"><span data-stu-id="5278d-125">Select the requester.</span></span>
    * <span data-ttu-id="5278d-126">“准备人”列表显示有权代表左窗格中选择的申请人订购物料的人员。</span><span class="sxs-lookup"><span data-stu-id="5278d-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>   <span data-ttu-id="5278d-127">您可以在此处添加更多准备人。</span><span class="sxs-lookup"><span data-stu-id="5278d-127">You can add additional preparers here.</span></span>   <span data-ttu-id="5278d-128">此视图还可用于为申请人授予在非该人的主法人或运营单位的法人和营运单位中创建申请的权限。</span><span class="sxs-lookup"><span data-stu-id="5278d-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  


