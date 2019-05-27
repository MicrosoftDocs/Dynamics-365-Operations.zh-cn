---
title: 在工作流中委托工作项
description: 如果您计划外出一段时间或无法对工作项进行操作，则您可以将您的工作项委托或重新分配给其他用户。
author: jasongre
manager: AnnBe
ms.date: 04/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: feace647d7acef6abf86b13fcb8019c622c55ff6
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509444"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="eb89f-103">在工作流中委托工作项</span><span class="sxs-lookup"><span data-stu-id="eb89f-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="eb89f-104">手动委托工作项</span><span class="sxs-lookup"><span data-stu-id="eb89f-104">Manually delegate a work item</span></span>

<span data-ttu-id="eb89f-105">若要委托单个工作项，请在**工作流**菜单中选择**委托**选项，然后输入要委托给的用户和注释。</span><span class="sxs-lookup"><span data-stu-id="eb89f-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="eb89f-106">这将把该工作项重新分配给该用户，以便该用户完成此工作项。</span><span class="sxs-lookup"><span data-stu-id="eb89f-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="eb89f-107">自动委托工作项</span><span class="sxs-lookup"><span data-stu-id="eb89f-107">Automatically delegate work items</span></span>

<span data-ttu-id="eb89f-108">如果您计划外出或一段时间无法对工作项进行操作，可以使用**用户选项**页面将新工作项自动委托给其他用户。</span><span class="sxs-lookup"><span data-stu-id="eb89f-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="eb89f-109">设置自动委托</span><span class="sxs-lookup"><span data-stu-id="eb89f-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="eb89f-110">转到“常规 > 设置 > 用户选项”。</span><span class="sxs-lookup"><span data-stu-id="eb89f-110">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="eb89f-111">单击“工作流”选项卡。</span><span class="sxs-lookup"><span data-stu-id="eb89f-111">Click the Workflow tab.</span></span>
    * <span data-ttu-id="eb89f-112">确保已展开“委托”部分。</span><span class="sxs-lookup"><span data-stu-id="eb89f-112">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="eb89f-113">要将系统配置为自动将您的工作项委托给其他用户，则您必须创建委托规则，指定何时委托特定类型的工作项。</span><span class="sxs-lookup"><span data-stu-id="eb89f-113">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="eb89f-114">按照以下步骤创建委托规则。</span><span class="sxs-lookup"><span data-stu-id="eb89f-114">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="eb89f-115">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="eb89f-115">Click Add.</span></span>
4. <span data-ttu-id="eb89f-116">在“范围”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="eb89f-116">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="eb89f-117">“所有”- 委托所有分配给您的所有工作项。</span><span class="sxs-lookup"><span data-stu-id="eb89f-117">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="eb89f-118">模块 – 仅委托与特定类型的工作流有关的工作项。</span><span class="sxs-lookup"><span data-stu-id="eb89f-118">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="eb89f-119">如果您选择此选项，则必须在“名称”字段中选择工作流的类型。</span><span class="sxs-lookup"><span data-stu-id="eb89f-119">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="eb89f-120">工作流 – 仅委托与特定工作流有关的工作项。</span><span class="sxs-lookup"><span data-stu-id="eb89f-120">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="eb89f-121">如果您选择此选项，则必须在“名称”字段中选择工作流。</span><span class="sxs-lookup"><span data-stu-id="eb89f-121">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="eb89f-122">在“委托”字段中，选择要将工作项委托给的用户。</span><span class="sxs-lookup"><span data-stu-id="eb89f-122">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="eb89f-123">使用“开始日期/时间”和“结束日期/时间”字段指定希望自动委托工作项的时间。</span><span class="sxs-lookup"><span data-stu-id="eb89f-123">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="eb89f-124">在“开始日期/时间”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="eb89f-124">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="eb89f-125">在“结束日期/时间”字段中输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="eb89f-125">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="eb89f-126">选中“启用”复选框以启用该委托规则。</span><span class="sxs-lookup"><span data-stu-id="eb89f-126">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="eb89f-127">如果已将“模块”选择为“范围”，则必须在“名称”字段中选择该模块。</span><span class="sxs-lookup"><span data-stu-id="eb89f-127">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="eb89f-128">如果已将“工作流”选择为“范围”，则必须在“名称”字段中选择要委托的具体工作流。</span><span class="sxs-lookup"><span data-stu-id="eb89f-128">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="eb89f-129">在“注释”字段中，输入说明您委托工作项的原因的注释。</span><span class="sxs-lookup"><span data-stu-id="eb89f-129">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>

