---
title: 确定和解决职责划分冲突
description: 您可以设置规则，以分离必须由不同用户执行的任务。
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d4a6bd14090213cc19a072d030bc26886c7a8d0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "353095"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a><span data-ttu-id="8c3b4-103">确定和解决职责划分冲突</span><span class="sxs-lookup"><span data-stu-id="8c3b4-103">Identify and resolve conflicts in segregation of duties</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8c3b4-104">您可以设置规则，以分离必须由不同用户执行的任务。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="8c3b4-105">此概念被称作职责划分。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="8c3b4-106">当安全角色定义或用户的角色分配违反规则时，会记录冲突。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-106">When the definition of a security role or the role assignments of a user violate the rules, the conflict is logged.</span></span> <span data-ttu-id="8c3b4-107">所有冲突必须由管理员解决。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-107">All conflicts must be resolved by the administrator.</span></span> <span data-ttu-id="8c3b4-108">完成以下过程以确定和解决冲突。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-108">Complete the following procedure to identify and resolve conflicts.</span></span> <span data-ttu-id="8c3b4-109">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-109">The demo data company used to create this procedure is USMF.</span></span>


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="8c3b4-110">核实用户角色分配是否符合新的职责划分规则</span><span class="sxs-lookup"><span data-stu-id="8c3b4-110">Verify whether user role assignments comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="8c3b4-111">转到“系统管理”>“安全”>“职责划分”>“核实用户角色分配的合规性”。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-111">Go to System administration > Security > Segregation of duties > Verify compliance of user-role assignments.</span></span>
2. <span data-ttu-id="8c3b4-112">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-112">Click OK.</span></span>
    * <span data-ttu-id="8c3b4-113">通知会显示核实结果。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-113">A notification displays the results of the validation.</span></span>     <span data-ttu-id="8c3b4-114"> 如果存在冲突，您可以打开“用户”页面，然后更改用户的角色分配。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-114">If there is a conflict, you can open the Users page and change the user’s role assignments.</span></span> <span data-ttu-id="8c3b4-115">此外，职责划分冲突页面也会记录冲突。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-115">Conflicts are also logged on the Segregation of duties conflicts page.</span></span>     <span data-ttu-id="8c3b4-116">要运行核实流程作为批处理作业，选择批处理，然后设置其他批处理参数。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-116">To run the verification process as a batch job, select Batch processing, and then set the other batch parameters.</span></span> <span data-ttu-id="8c3b4-117">在批处理作业运行之后，您可以审查职责划分冲突页面上的冲突。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-117">After the batch job runs, you can review the conflicts in the Segregation of duties conflicts page.</span></span>  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a><span data-ttu-id="8c3b4-118">查看并解决存在冲突的用户角色分配</span><span class="sxs-lookup"><span data-stu-id="8c3b4-118">View and resolve conflicting user role assignments</span></span>
1. <span data-ttu-id="8c3b4-119">转到“系统管理”>“安全”>“职责划分”>“职责划分冲突”。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-119">Go to System administration > Security > Segregation of duties > Segregation of duties conflicts.</span></span>
    * <span data-ttu-id="8c3b4-120">选择某一冲突，然后单击以下按钮之一：     拒绝分配 - 拒绝分配给该用户其他的安全角色。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-120">Select a conflict, and then click one of the following buttons:     Deny assignment – Deny the assignment of the user to the additional security role.</span></span> <span data-ttu-id="8c3b4-121">如果您拒绝自动角色分配，用户会被标记为从角色中排除。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-121">If you deny an automatic role assignment, the user is marked as excluded from the role.</span></span> <span data-ttu-id="8c3b4-122">被排除的用户不会被授予与该角色关联的访问权限，并且该用户不会被分配角色，直到管理员删除排除。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-122">The excluded user is not granted the access that is associated with the role, and the user cannot be assigned to the role until the administrator removes the exclusion.</span></span>     <span data-ttu-id="8c3b4-123"> 允许分配 – 覆盖冲突，并允许分配给用户两个安全角色。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-123">Allow assignment – Override the conflict, and allow the user to be assigned to both security roles.</span></span> <span data-ttu-id="8c3b4-124">如果您覆盖冲突，您必须在“覆盖原因”字段中输入原因。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-124">If you override a conflict, you must enter a reason in the Reason for override field.</span></span>  
2. <span data-ttu-id="8c3b4-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-125">Close the page.</span></span>
3. <span data-ttu-id="8c3b4-126">转到“系统管理”>“安全”>“职责划分”>“职责划分未解决的冲突”。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-126">Go to System administration > Security > Segregation of duties > Segregation of duties unresolved conflicts.</span></span>
    * <span data-ttu-id="8c3b4-127">选择某一冲突，然后单击以下按钮之一：     拒绝分配 - 拒绝分配给该用户其他的安全角色。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-127">Select a conflict, and then click one of the following buttons:     Deny assignment – Deny the assignment of the user to the additional security role.</span></span> <span data-ttu-id="8c3b4-128">如果您拒绝自动角色分配，用户会被标记为从角色中排除。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-128">If you deny an automatic role assignment, the user is marked as excluded from the role.</span></span> <span data-ttu-id="8c3b4-129">被排除的用户不会被授予与该角色关联的访问权限，并且该用户不会被分配角色，直到管理员删除排除。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-129">The excluded user is not granted the access that is associated with the role, and the user cannot be assigned to the role until the administrator removes the exclusion.</span></span>     <span data-ttu-id="8c3b4-130"> 允许分配 – 覆盖冲突，并允许分配给用户两个安全角色。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-130">Allow assignment – Override the conflict, and allow the user to be assigned to both security roles.</span></span> <span data-ttu-id="8c3b4-131">如果您覆盖冲突，您必须在“覆盖原因”字段中输入原因。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-131">If you override a conflict, you must enter a reason in the Reason for override field.</span></span>    
4. <span data-ttu-id="8c3b4-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-132">Close the page.</span></span>

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="8c3b4-133">核实现有角色是否符合新的职责划分规则</span><span class="sxs-lookup"><span data-stu-id="8c3b4-133">Verify whether existing roles comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="8c3b4-134">转到“系统管理”>“安全”>“职责划分”>“职责划分规则”。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-134">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
    * <span data-ttu-id="8c3b4-135">选择一个规则。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-135">Select a rule.</span></span>  
2. <span data-ttu-id="8c3b4-136">单击“核实职责和角色”。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-136">Click Validate duties and roles.</span></span>
    * <span data-ttu-id="8c3b4-137">如果任何现有角色违反选定的规则，会显示包含角色名称和冲突职责的名称。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-137">If any existing roles violate the selected rule, a message is displayed that contains the name of the role and the names of the conflicting duties.</span></span> <span data-ttu-id="8c3b4-138">管理员必须指明减少安全风险或修改角色，以确保不违反职责划分规则。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-138">The administrator must either indicate the mitigation for the security risk or modify the role so that it does not violate the rules for segregation of duties.</span></span>     <span data-ttu-id="8c3b4-139"> 如果没有角色违反选定的规则，会显示一条消息，以指明所有角色都遵从规则。</span><span class="sxs-lookup"><span data-stu-id="8c3b4-139">If no roles violate the selected rule, a message indicates that all roles are in compliance.</span></span>  

