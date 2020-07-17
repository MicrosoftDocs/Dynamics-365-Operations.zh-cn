---
title: 在工作流中委托工作项
description: 如果您计划外出一段时间或无法对工作项进行操作，则您可以将您的工作项委托或重新分配给其他用户。
author: ChrisGarty
manager: AnnBe
ms.date: 06/23/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d98d84b89f1f3322a9c896b74b63a3b6425b13b
ms.sourcegitcommit: 267864eb0dccd6e26d49d280bd4ad1b770a73a77
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "3515756"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="dc8da-103">在工作流中委托工作项</span><span class="sxs-lookup"><span data-stu-id="dc8da-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="dc8da-104">手动委托工作项</span><span class="sxs-lookup"><span data-stu-id="dc8da-104">Manually delegate a work item</span></span>

<span data-ttu-id="dc8da-105">若要委托单个工作项，请在**工作流**菜单中选择**委托**选项，然后输入要委托给的用户和注释。</span><span class="sxs-lookup"><span data-stu-id="dc8da-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="dc8da-106">这将把该工作项重新分配给该用户，以便该用户完成此工作项。</span><span class="sxs-lookup"><span data-stu-id="dc8da-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="dc8da-107">手动委托多个工作项</span><span class="sxs-lookup"><span data-stu-id="dc8da-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="dc8da-108">可以从**分配给我的工作项**页一并委托多个工作项。</span><span class="sxs-lookup"><span data-stu-id="dc8da-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="dc8da-109">以下工作流类型支持批量委托：采购协议审核工作流、采购订单工作流、采购申请审核和供应商账单工作流。</span><span class="sxs-lookup"><span data-stu-id="dc8da-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="dc8da-110">**委托多个工作项**功能默认已禁用，可以在**工作区 > 功能管理**中启用。</span><span class="sxs-lookup"><span data-stu-id="dc8da-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="dc8da-111">请与系统管理员联系，获取启用此功能的帮助。</span><span class="sxs-lookup"><span data-stu-id="dc8da-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="dc8da-112">转到**通用 > 通用 > 工作项 > 分配给我的工作项**。</span><span class="sxs-lookup"><span data-stu-id="dc8da-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="dc8da-113">选择将委托的工作项。</span><span class="sxs-lookup"><span data-stu-id="dc8da-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="dc8da-114">单击**委托工作项**菜单。</span><span class="sxs-lookup"><span data-stu-id="dc8da-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="dc8da-115">在**用户**字段中，选择要将工作项委托给的用户。</span><span class="sxs-lookup"><span data-stu-id="dc8da-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="dc8da-116">在**注释**字段中，输入说明您委托工作项的原因的注释。</span><span class="sxs-lookup"><span data-stu-id="dc8da-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="dc8da-117">单击**委托工作项**按钮完成工作项委托。</span><span class="sxs-lookup"><span data-stu-id="dc8da-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="dc8da-118">自动委托工作项</span><span class="sxs-lookup"><span data-stu-id="dc8da-118">Automatically delegate work items</span></span>

<span data-ttu-id="dc8da-119">如果您计划外出或一段时间无法对工作项进行操作，可以使用**用户选项**页面将新工作项自动委托给其他用户。</span><span class="sxs-lookup"><span data-stu-id="dc8da-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="dc8da-120">设置自动委托</span><span class="sxs-lookup"><span data-stu-id="dc8da-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="dc8da-121">转到**常规 > 设置 > 用户选项**。</span><span class="sxs-lookup"><span data-stu-id="dc8da-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="dc8da-122">单击**工作流**选项卡。确保展开“委托”部分。</span><span class="sxs-lookup"><span data-stu-id="dc8da-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="dc8da-123">要将系统配置为自动将您的工作项委托给其他用户，则您必须创建委托规则，指定何时委托特定类型的工作项。</span><span class="sxs-lookup"><span data-stu-id="dc8da-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="dc8da-124">按照以下步骤创建委托规则。</span><span class="sxs-lookup"><span data-stu-id="dc8da-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="dc8da-125">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="dc8da-125">Click **Add**.</span></span>
4. <span data-ttu-id="dc8da-126">在**范围**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="dc8da-126">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="dc8da-127">“所有”- 委托所有分配给您的所有工作项。</span><span class="sxs-lookup"><span data-stu-id="dc8da-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="dc8da-128">模块 – 仅委托与特定类型的工作流有关的工作项。</span><span class="sxs-lookup"><span data-stu-id="dc8da-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="dc8da-129">如果您选择此选项，则必须在“名称”字段中选择工作流的类型。</span><span class="sxs-lookup"><span data-stu-id="dc8da-129">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="dc8da-130">工作流 – 仅委托与特定工作流有关的工作项。</span><span class="sxs-lookup"><span data-stu-id="dc8da-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="dc8da-131">如果您选择此选项，则必须在“名称”字段中选择工作流。</span><span class="sxs-lookup"><span data-stu-id="dc8da-131">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="dc8da-132">在**委托**字段中，选择要将工作项委托给的用户。</span><span class="sxs-lookup"><span data-stu-id="dc8da-132">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="dc8da-133">使用“开始日期/时间”和“结束日期/时间”字段指定希望自动委托工作项的时间。</span><span class="sxs-lookup"><span data-stu-id="dc8da-133">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="dc8da-134">在**开始日期/时间**字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="dc8da-134">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="dc8da-135">在**结束日期/时间**字段中输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="dc8da-135">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="dc8da-136">选中**启用**复选框以启用该委托规则。</span><span class="sxs-lookup"><span data-stu-id="dc8da-136">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="dc8da-137">如果已将**模块**选择为“范围”，则必须在“名称”字段中选择该模块。</span><span class="sxs-lookup"><span data-stu-id="dc8da-137">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="dc8da-138">如果已将**工作流**选择为“范围”，则必须在“名称”字段中选择要委托的具体工作流。</span><span class="sxs-lookup"><span data-stu-id="dc8da-138">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="dc8da-139">在**注释**字段中，输入说明您委托工作项的原因的注释。</span><span class="sxs-lookup"><span data-stu-id="dc8da-139">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>

