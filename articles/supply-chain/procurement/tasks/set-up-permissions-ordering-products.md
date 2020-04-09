---
title: 代表他人设置产品订购权限
description: 此主题介绍如何为工作人员授予代表其他工作人员起草采购申请的权限。
author: mkirknel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe8ad0540febcc703554e2451f7f644338e4d57b
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149450"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="edc6a-103">代表他人设置产品订购权限</span><span class="sxs-lookup"><span data-stu-id="edc6a-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="edc6a-104">此主题介绍如何为工作人员授予代表其他工作人员起草采购申请的权限。</span><span class="sxs-lookup"><span data-stu-id="edc6a-104">This topic explains how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="edc6a-105">换句话说，采购申请“准备人”可以为其他“申请人”创建申请。</span><span class="sxs-lookup"><span data-stu-id="edc6a-105">In other words, a purchase requisition "preparer" can create a requisition for another "requester."</span></span> <span data-ttu-id="edc6a-106">此过程还演示如何为工作人员授予在不同法人或营运单位中订购物料和服务的权限。</span><span class="sxs-lookup"><span data-stu-id="edc6a-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="edc6a-107">这些任务通常由采购经理执行。</span><span class="sxs-lookup"><span data-stu-id="edc6a-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="edc6a-108">您可以在此过程中使用 USMF 演示数据公司的数据，也可以使用您自己的数据。</span><span class="sxs-lookup"><span data-stu-id="edc6a-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="edc6a-109">授予代表其他工作人员输入采购申请的权限</span><span class="sxs-lookup"><span data-stu-id="edc6a-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="edc6a-110">在导航窗格中，转到**模块 > 采购 > 设置 > 策略 > 采购申请权限**。</span><span class="sxs-lookup"><span data-stu-id="edc6a-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchase requisition permissions**.</span></span> <span data-ttu-id="edc6a-111">确保**当前视图**字段设置为**按准备人**。</span><span class="sxs-lookup"><span data-stu-id="edc6a-111">Make sure that the **Current view** field is set to **By preparer**.</span></span> <span data-ttu-id="edc6a-112">左窗格中的列表显示已授予为代表其他人起草申请的权限的人员。</span><span class="sxs-lookup"><span data-stu-id="edc6a-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="edc6a-113">选择要为其授予（准备人）权限的人员。</span><span class="sxs-lookup"><span data-stu-id="edc6a-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="edc6a-114">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="edc6a-114">Select **Add**.</span></span>
4. <span data-ttu-id="edc6a-115">找到并选择要添加为申请人的人员。</span><span class="sxs-lookup"><span data-stu-id="edc6a-115">Find and select the person to add as a requester.</span></span>
    - <span data-ttu-id="edc6a-116">申请人是可被准备人代表创建申请的人员。</span><span class="sxs-lookup"><span data-stu-id="edc6a-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    - <span data-ttu-id="edc6a-117">如果准备人应该可以代表所选工作人员创建采购申请，请在**授权**字段中选择**特定**。</span><span class="sxs-lookup"><span data-stu-id="edc6a-117">In the **Authorization** field, select **Specific** if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="edc6a-118">如果准备人还需要可以代表向工作人员报告的所有工作人员创建采购申请，请选择**报告**。</span><span class="sxs-lookup"><span data-stu-id="edc6a-118">Select **Reporting** if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="edc6a-119">在**生效日期**字段，输入日期。</span><span class="sxs-lookup"><span data-stu-id="edc6a-119">In the **Effective** field, enter a date.</span></span>
6. <span data-ttu-id="edc6a-120">在**截止日期**字段，输入日期。</span><span class="sxs-lookup"><span data-stu-id="edc6a-120">In the **Expiration** field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="edc6a-121">查看有权为所选工作人员创建采购申请的准备人</span><span class="sxs-lookup"><span data-stu-id="edc6a-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="edc6a-122">在**当前视图**字段中，选择**按申请人**。</span><span class="sxs-lookup"><span data-stu-id="edc6a-122">In the **Current view** field, select **By requester**.</span></span> <span data-ttu-id="edc6a-123">此视图显示已授予为代表所选工作人员创建采购业务申请权限的准备人列表。</span><span class="sxs-lookup"><span data-stu-id="edc6a-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="edc6a-124">使用快速筛选器查找您刚才添加为申请人的工作人员。</span><span class="sxs-lookup"><span data-stu-id="edc6a-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="edc6a-125">选择该申请人。</span><span class="sxs-lookup"><span data-stu-id="edc6a-125">Select the requester.</span></span> <span data-ttu-id="edc6a-126">“准备人”列表显示有权代表左窗格中选择的申请人订购物料的人员。</span><span class="sxs-lookup"><span data-stu-id="edc6a-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>  <span data-ttu-id="edc6a-127">您可以在此处添加更多准备人。</span><span class="sxs-lookup"><span data-stu-id="edc6a-127">You can add additional preparers here.</span></span> <span data-ttu-id="edc6a-128">此视图还可用于为申请人授予在非该人的主法人或运营单位的法人和营运单位中创建申请的权限。</span><span class="sxs-lookup"><span data-stu-id="edc6a-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  

