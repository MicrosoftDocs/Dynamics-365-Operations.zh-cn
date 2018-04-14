--- 
title: "在工作流中委托工作项"
description: "如果您计划外出一段时间或无法对工作项进行操作，则您可以将您的工作项委托或重新分配给其他用户。"
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: cd3d09ed12fa4419881910884acefaf1bf5fa0d4
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="7978b-103">在工作流中委托工作项</span><span class="sxs-lookup"><span data-stu-id="7978b-103">Delegate work items in a workflow</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7978b-104">如果您计划外出一段时间或无法对工作项进行操作，则您可以将您的工作项委托或重新分配给其他用户。</span><span class="sxs-lookup"><span data-stu-id="7978b-104">If you plan to be out of the office or otherwise unavailable to act on work items, you can delegate, or reassign, your work items to other users.</span></span> <span data-ttu-id="7978b-105">此过程帮助您配置系统以自动将您的工作项委托给其他用户。</span><span class="sxs-lookup"><span data-stu-id="7978b-105">This procedure helps you configure the system to automatically delegate your work items to another user.</span></span>



<span data-ttu-id="7978b-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="7978b-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-automatic-delegation"></a><span data-ttu-id="7978b-107">设置自动委托</span><span class="sxs-lookup"><span data-stu-id="7978b-107">Set up automatic delegation</span></span>
1. <span data-ttu-id="7978b-108">转到“常规 > 设置 > 用户选项”。</span><span class="sxs-lookup"><span data-stu-id="7978b-108">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="7978b-109">单击“工作流”选项卡。</span><span class="sxs-lookup"><span data-stu-id="7978b-109">Click the Workflow tab.</span></span>
    * <span data-ttu-id="7978b-110">确保已展开“委托”部分。</span><span class="sxs-lookup"><span data-stu-id="7978b-110">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="7978b-111">要将系统配置为自动将您的工作项委托给其他用户，则您必须创建委托规则，指定何时委托特定类型的工作项。</span><span class="sxs-lookup"><span data-stu-id="7978b-111">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="7978b-112">按照以下步骤创建委托规则。</span><span class="sxs-lookup"><span data-stu-id="7978b-112">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="7978b-113">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="7978b-113">Click Add.</span></span>
4. <span data-ttu-id="7978b-114">在“范围”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="7978b-114">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="7978b-115">“所有”- 委托所有分配给您的所有工作项。</span><span class="sxs-lookup"><span data-stu-id="7978b-115">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="7978b-116">模块 – 仅委托与特定类型的工作流有关的工作项。</span><span class="sxs-lookup"><span data-stu-id="7978b-116">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="7978b-117">如果您选择此选项，则必须在“名称”字段中选择工作流的类型。</span><span class="sxs-lookup"><span data-stu-id="7978b-117">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="7978b-118">工作流 – 仅委托与特定工作流有关的工作项。</span><span class="sxs-lookup"><span data-stu-id="7978b-118">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="7978b-119">如果您选择此选项，则必须在“名称”字段中选择工作流。</span><span class="sxs-lookup"><span data-stu-id="7978b-119">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="7978b-120">在“委托”字段中，选择要将工作项委托给的用户。</span><span class="sxs-lookup"><span data-stu-id="7978b-120">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="7978b-121">使用“开始日期/时间”和“结束日期/时间”字段指定希望自动委托工作项的时间。</span><span class="sxs-lookup"><span data-stu-id="7978b-121">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="7978b-122">在“开始日期/时间”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="7978b-122">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="7978b-123">在“结束日期/时间”字段中输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="7978b-123">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="7978b-124">选中“启用”复选框以启用该委托规则。</span><span class="sxs-lookup"><span data-stu-id="7978b-124">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="7978b-125">如果已将“模块”选择为“范围”，则必须在“名称”字段中选择该模块。</span><span class="sxs-lookup"><span data-stu-id="7978b-125">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="7978b-126">如果已将“工作流”选择为“范围”，则必须在“名称”字段中选择要委托的具体工作流。</span><span class="sxs-lookup"><span data-stu-id="7978b-126">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="7978b-127">在“注释”字段中，输入说明您委托工作项的原因的注释。</span><span class="sxs-lookup"><span data-stu-id="7978b-127">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>


