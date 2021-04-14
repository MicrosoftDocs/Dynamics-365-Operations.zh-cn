---
title: 确定和解决职责划分冲突
description: 本主题介绍如何确定和解决职责划分冲突。
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ebd59c7018a50e01253697d792698664a981566
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745805"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a><span data-ttu-id="84d99-103">确定和解决职责划分冲突</span><span class="sxs-lookup"><span data-stu-id="84d99-103">Identify and resolve conflicts in segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="84d99-104">本主题介绍如何确定和解决职责划分冲突。</span><span class="sxs-lookup"><span data-stu-id="84d99-104">This topic explains how to identify and resolve conflicts in segregation of duties.</span></span> <span data-ttu-id="84d99-105">您可以设置规则，以分离必须由不同用户执行的职责。</span><span class="sxs-lookup"><span data-stu-id="84d99-105">You can set up rules to separate duties that must be performed by different users.</span></span> <span data-ttu-id="84d99-106">此概念被称作职责划分。</span><span class="sxs-lookup"><span data-stu-id="84d99-106">This concept is named segregation of duties.</span></span> <span data-ttu-id="84d99-107">当安全角色定义或用户的角色分配违反规则时，会记录冲突。</span><span class="sxs-lookup"><span data-stu-id="84d99-107">When the definition of a security role or the role assignments of a user violate the rules, the conflict is logged.</span></span> <span data-ttu-id="84d99-108">所有冲突必须由管理员解决。</span><span class="sxs-lookup"><span data-stu-id="84d99-108">All conflicts must be resolved by the administrator.</span></span> <span data-ttu-id="84d99-109">完成以下过程以确定和解决冲突。</span><span class="sxs-lookup"><span data-stu-id="84d99-109">Complete the following procedure to identify and resolve conflicts.</span></span>

<span data-ttu-id="84d99-110">添加规则后，请验证所有现有角色是否符合规则。</span><span class="sxs-lookup"><span data-stu-id="84d99-110">After a rule has been added, verify that all existing roles are compliant.</span></span> 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="84d99-111">验证现有角色和职责是否符合新的职责划分规则</span><span class="sxs-lookup"><span data-stu-id="84d99-111">Verify that existing roles and duties comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="84d99-112">转到 **系统管理** > **安全** > **职责划分** > **职责划分规则**。</span><span class="sxs-lookup"><span data-stu-id="84d99-112">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
3. <span data-ttu-id="84d99-113">选择 **验证职责和角色**。</span><span class="sxs-lookup"><span data-stu-id="84d99-113">Select **Validate duties and roles**.</span></span> <span data-ttu-id="84d99-114">如果任何角色违反规则，会显示包含规则名称、角色和冲突职责的名称的消息。</span><span class="sxs-lookup"><span data-stu-id="84d99-114">If any roles violate the rules, a message is displayed that contains the name of the rule, the role, and the names of the conflicting duties.</span></span> <span data-ttu-id="84d99-115">冲突角色必须使用 **安全配置** 修改，并且不能包含冲突职责。</span><span class="sxs-lookup"><span data-stu-id="84d99-115">Conflicting roles must be modified using **Security configuration** and can't include conflicting duties.</span></span> <span data-ttu-id="84d99-116">如果没有角色违反选定的规则，会显示一条消息，以指明所有角色都符合规则。</span><span class="sxs-lookup"><span data-stu-id="84d99-116">If no roles violate the selected rule, a message indicates that all roles comply.</span></span>   

> [!NOTE]
> <span data-ttu-id="84d99-117">验证仅针对所选规则执行。</span><span class="sxs-lookup"><span data-stu-id="84d99-117">The validation is only performed for the selected rule.</span></span> <span data-ttu-id="84d99-118">验证对每个规则的合规性很重要。</span><span class="sxs-lookup"><span data-stu-id="84d99-118">It is important to validate compliance for each rule.</span></span>   

<span data-ttu-id="84d99-119">创建或修改角色时，会自动执行职责划分规则。</span><span class="sxs-lookup"><span data-stu-id="84d99-119">When you create or modify a role, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="84d99-120">您无法为角色分配冲突职责。</span><span class="sxs-lookup"><span data-stu-id="84d99-120">You cannot assign conflicting duties to a role.</span></span>

<span data-ttu-id="84d99-121">接下来，验证所有现有角色分配均符合规则。</span><span class="sxs-lookup"><span data-stu-id="84d99-121">Next, verify that all existing role assignments are compliant.</span></span>

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="84d99-122">验证用户角色分配是否符合新的职责划分规则</span><span class="sxs-lookup"><span data-stu-id="84d99-122">Verify that user role assignments comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="84d99-123">转到 **系统管理 > 安全 > 职责划分 > 验证用户角色分配的合规性**。</span><span class="sxs-lookup"><span data-stu-id="84d99-123">Go to **System administration > Security > Segregation of duties > Verify compliance of user-role assignments**.</span></span>
2. <span data-ttu-id="84d99-124">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="84d99-124">Select **OK**.</span></span> <span data-ttu-id="84d99-125">通知会显示核实结果。</span><span class="sxs-lookup"><span data-stu-id="84d99-125">A notification displays the results of the validation.</span></span> <span data-ttu-id="84d99-126">**职责划分未解决的冲突** 页会记录冲突。</span><span class="sxs-lookup"><span data-stu-id="84d99-126">Conflicts are logged on the **Segregation of duties unresolved conflicts** page.</span></span>   

<span data-ttu-id="84d99-127">将用户分配给角色时，会自动执行职责划分规则。</span><span class="sxs-lookup"><span data-stu-id="84d99-127">When you assign users to roles, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="84d99-128">如果您尝试将用户分配给包含冲突职责的角色，会收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="84d99-128">If you try to assign a user to roles that contain conflicting duties, you receive an error message.</span></span> <span data-ttu-id="84d99-129">然后，您必须通过拒绝或允许其他角色分配来解决冲突。</span><span class="sxs-lookup"><span data-stu-id="84d99-129">You must then resolve the conflict by denying or allowing the additional role assignment.</span></span> <span data-ttu-id="84d99-130">允许分配后，将分配其他角色。</span><span class="sxs-lookup"><span data-stu-id="84d99-130">The additional role will be assigned after the assignment is allowed.</span></span> 

> [!NOTE]
> <span data-ttu-id="84d99-131">当前不对基于 Active Directory 域组分配了角色的用户验证冲突。</span><span class="sxs-lookup"><span data-stu-id="84d99-131">Conflicts are currently not verified for users that are assigned roles based on the Active Directory Domain groups.</span></span>

## <a name="view-and-resolve-conflicting-user-role-assignments"></a><span data-ttu-id="84d99-132">查看并解决存在冲突的用户角色分配</span><span class="sxs-lookup"><span data-stu-id="84d99-132">View and resolve conflicting user role assignments</span></span>
1. <span data-ttu-id="84d99-133">转到 **系统管理** > **安全** > **职责划分** > **职责划分未解决的冲突**。</span><span class="sxs-lookup"><span data-stu-id="84d99-133">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties unresolved conflicts**.</span></span> 
2. <span data-ttu-id="84d99-134">选择某一冲突，然后选择以下操作之一：</span><span class="sxs-lookup"><span data-stu-id="84d99-134">Select a conflict, and then select one of the following actions:</span></span> 

  - <span data-ttu-id="84d99-135">**拒绝分配**：这将拒绝分配给该用户其他的安全角色。</span><span class="sxs-lookup"><span data-stu-id="84d99-135">**Deny assignment**: This will deny the assignment of the user to the additional security role.</span></span> <span data-ttu-id="84d99-136">如果您拒绝自动角色分配，用户会被标记为从角色中排除。</span><span class="sxs-lookup"><span data-stu-id="84d99-136">If you deny an automatic role assignment, the user is marked as excluded from the role.</span></span> <span data-ttu-id="84d99-137">被排除的用户不会被授予与该角色关联的访问权限，并且不会被分配角色，直到管理员删除排除。</span><span class="sxs-lookup"><span data-stu-id="84d99-137">The excluded user isn't granted the access associated with the role and can't be assigned to the role until the administrator removes the exclusion.</span></span> 
-  <span data-ttu-id="84d99-138">**允许分配**：这将覆盖冲突，并允许分配给用户其他安全角色。</span><span class="sxs-lookup"><span data-stu-id="84d99-138">**Allow assignment**: This will override the conflict and allow the user to be assigned to the additional security role.</span></span> <span data-ttu-id="84d99-139">如果您覆盖冲突，您必须在 **覆盖原因** 字段中输入原因。</span><span class="sxs-lookup"><span data-stu-id="84d99-139">If you override a conflict, you must enter a reason in the **Reason for override** field.</span></span> <span data-ttu-id="84d99-140">所有被覆盖的角色分配可以在 **职责划分冲突** 页上查看。</span><span class="sxs-lookup"><span data-stu-id="84d99-140">All overridden role assignments can be viewed on the **Segregation of duties conflicts** page.</span></span>  

> [!NOTE]
> <span data-ttu-id="84d99-141">如果为同一用户列出了多个冲突，在 **用户** 页上选择用户记录并评估分配的角色。</span><span class="sxs-lookup"><span data-stu-id="84d99-141">If several conflicts are listed for the same user, select the user record and evaluate assigned roles on the **Users** page.</span></span> <span data-ttu-id="84d99-142">为避免这一冲突，请在添加或修改每个规则后对其进行验证。</span><span class="sxs-lookup"><span data-stu-id="84d99-142">To avoid this conflict, validate each rule after it's added or modified.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]