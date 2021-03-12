---
title: 在工作流中委托工作项
description: 如果您计划外出一段时间或无法对工作项进行操作，则您可以将您的工作项委托或重新分配给其他用户。
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48d8fd06217d318fa8208e11ffa5624f6be25be1
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796698"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="54cef-103">在工作流中委托工作项</span><span class="sxs-lookup"><span data-stu-id="54cef-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="54cef-104">手动委托工作项</span><span class="sxs-lookup"><span data-stu-id="54cef-104">Manually delegate a work item</span></span>

<span data-ttu-id="54cef-105">若要委托单个工作项，请在 **工作流** 菜单中选择 **委托** 选项，然后输入要委托给的用户和注释。</span><span class="sxs-lookup"><span data-stu-id="54cef-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="54cef-106">这将把该工作项重新分配给该用户，以便该用户完成此工作项。</span><span class="sxs-lookup"><span data-stu-id="54cef-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="54cef-107">手动委托多个工作项</span><span class="sxs-lookup"><span data-stu-id="54cef-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="54cef-108">可以从 **分配给我的工作项** 页一并委托多个工作项。</span><span class="sxs-lookup"><span data-stu-id="54cef-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="54cef-109">以下工作流类型支持批量委托：采购协议审核工作流、采购订单工作流、采购申请审核和供应商账单工作流。</span><span class="sxs-lookup"><span data-stu-id="54cef-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="54cef-110">**委托多个工作项** 功能默认已禁用，可以在 **工作区 > 功能管理** 中启用。</span><span class="sxs-lookup"><span data-stu-id="54cef-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="54cef-111">请与系统管理员联系，获取启用此功能的帮助。</span><span class="sxs-lookup"><span data-stu-id="54cef-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="54cef-112">转到 **通用 > 通用 > 工作项 > 分配给我的工作项**。</span><span class="sxs-lookup"><span data-stu-id="54cef-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="54cef-113">选择将委托的工作项。</span><span class="sxs-lookup"><span data-stu-id="54cef-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="54cef-114">单击 **委托工作项** 菜单。</span><span class="sxs-lookup"><span data-stu-id="54cef-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="54cef-115">在 **用户** 字段中，选择要将工作项委托给的用户。</span><span class="sxs-lookup"><span data-stu-id="54cef-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="54cef-116">在 **注释** 字段中，输入说明您委托工作项的原因的注释。</span><span class="sxs-lookup"><span data-stu-id="54cef-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="54cef-117">单击 **委托工作项** 按钮完成工作项委托。</span><span class="sxs-lookup"><span data-stu-id="54cef-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="54cef-118">自动委托工作项</span><span class="sxs-lookup"><span data-stu-id="54cef-118">Automatically delegate work items</span></span>

<span data-ttu-id="54cef-119">如果您计划外出或一段时间无法对工作项进行操作，可以使用 **用户选项** 页面将新工作项自动委托给其他用户。</span><span class="sxs-lookup"><span data-stu-id="54cef-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="54cef-120">设置自动委托</span><span class="sxs-lookup"><span data-stu-id="54cef-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="54cef-121">转到 **常规 > 设置 > 用户选项**。</span><span class="sxs-lookup"><span data-stu-id="54cef-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="54cef-122">单击 **工作流** 选项卡。确保展开“委托”部分。</span><span class="sxs-lookup"><span data-stu-id="54cef-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="54cef-123">要将系统配置为自动将您的工作项委托给其他用户，则您必须创建委托规则，指定何时委托特定类型的工作项。</span><span class="sxs-lookup"><span data-stu-id="54cef-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="54cef-124">按照以下步骤创建委托规则。</span><span class="sxs-lookup"><span data-stu-id="54cef-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="54cef-125">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="54cef-125">Click **Add**.</span></span>
4. <span data-ttu-id="54cef-126">在 **范围** 字段中，选择一个选项：</span><span class="sxs-lookup"><span data-stu-id="54cef-126">In the **Scope** field, select an option:</span></span>
    - <span data-ttu-id="54cef-127">“所有”- 委托所有分配给您的所有工作项。</span><span class="sxs-lookup"><span data-stu-id="54cef-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="54cef-128">模块 – 仅委托与特定类型的工作流有关的工作项。</span><span class="sxs-lookup"><span data-stu-id="54cef-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="54cef-129">如果您选择此选项，则必须在 **名称** 字段中选择工作流的类型。</span><span class="sxs-lookup"><span data-stu-id="54cef-129">If you select this option, you must select the type of workflow in the **Name** field.</span></span>
    - <span data-ttu-id="54cef-130">工作流 – 仅委托与特定工作流有关的工作项。</span><span class="sxs-lookup"><span data-stu-id="54cef-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="54cef-131">如果您选择此选项，则必须在 **名称** 字段中选择工作流。</span><span class="sxs-lookup"><span data-stu-id="54cef-131">If you select this option, you must select the workflow in the **Name** field.</span></span>  
5. <span data-ttu-id="54cef-132">在 **名称** 字段中：</span><span class="sxs-lookup"><span data-stu-id="54cef-132">In the **Name** field:</span></span>
    - <span data-ttu-id="54cef-133">对于 **模块** 范围，选择目标模块。</span><span class="sxs-lookup"><span data-stu-id="54cef-133">For **Module** scope, select the target module.</span></span>
    - <span data-ttu-id="54cef-134">对于 **工作流** 范围，选择目标工作流。</span><span class="sxs-lookup"><span data-stu-id="54cef-134">For **Workflow** scope, select the target workflow.</span></span>
6. <span data-ttu-id="54cef-135">在 **委托** 字段中，选择要将工作项委托给的用户。</span><span class="sxs-lookup"><span data-stu-id="54cef-135">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="54cef-136">使用 **开始日期/时间** 和 **结束日期/时间** 字段指定希望自动委托工作项的时间。</span><span class="sxs-lookup"><span data-stu-id="54cef-136">Use the **Start date/time** and **End date/time** fields to specify when you want the work items to be automatically delegated.</span></span>  
7. <span data-ttu-id="54cef-137">在 **开始日期/时间** 字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="54cef-137">In the **Start date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="54cef-138">在 **结束日期/时间** 字段中输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="54cef-138">In the **End date/time** field, enter a date and time.</span></span>
9. <span data-ttu-id="54cef-139">选中 **启用** 复选框以启用该委托规则。</span><span class="sxs-lookup"><span data-stu-id="54cef-139">Select the **Enabled** check box to activate the delegation rule.</span></span> 
10. <span data-ttu-id="54cef-140">在 **注释** 字段中，输入说明您委托工作项的原因的注释。</span><span class="sxs-lookup"><span data-stu-id="54cef-140">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
