---
title: 配置成本对象控制器的访问权限
description: 此过程用于配置成本对象总监的访问权限。
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b7356706ea80c97fdf5b73faf32134a4aebacbb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841433"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="12ba7-103">配置成本对象控制器的访问权限</span><span class="sxs-lookup"><span data-stu-id="12ba7-103">Configure access rights for a cost object controller</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="12ba7-104">此过程用于配置成本对象总监的访问权限。</span><span class="sxs-lookup"><span data-stu-id="12ba7-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="12ba7-105">此录制使用 USP2 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="12ba7-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="12ba7-106">分配成本对象总监角色</span><span class="sxs-lookup"><span data-stu-id="12ba7-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="12ba7-107">转到“系统管理”>“用户”>“用户”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="12ba7-108">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="12ba7-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="12ba7-109">例如，在“用户名”字段中筛选值“alicia”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="12ba7-110">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="12ba7-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="12ba7-111">单击“分配角色”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-111">Click Assign roles.</span></span>
5. <span data-ttu-id="12ba7-112">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="12ba7-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="12ba7-113">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="12ba7-114">启用访问列表安全性</span><span class="sxs-lookup"><span data-stu-id="12ba7-114">Enable access list security</span></span>
1. <span data-ttu-id="12ba7-115">转到“成本核算”>“维度”>“维度层次结构”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="12ba7-116">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="12ba7-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="12ba7-117">选择“组织”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-117">Select Organization.</span></span>  
3. <span data-ttu-id="12ba7-118">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-118">Click Edit.</span></span>
4. <span data-ttu-id="12ba7-119">在“访问列表层次结构”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="12ba7-120">单击“查看层次结构”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="12ba7-121">为用户分配访问权限</span><span class="sxs-lookup"><span data-stu-id="12ba7-121">Assign access rights to user</span></span>
1. <span data-ttu-id="12ba7-122">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-122">Click New.</span></span>
2. <span data-ttu-id="12ba7-123">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="12ba7-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="12ba7-124">在“用户身份”字段，输入或选一个值。</span><span class="sxs-lookup"><span data-stu-id="12ba7-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="12ba7-125">选择“管理员”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-125">Select Admin.</span></span>  
4. <span data-ttu-id="12ba7-126">在树中，选择“组织\CEO\CFO\FIM”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="12ba7-127">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-127">Click New.</span></span>
6. <span data-ttu-id="12ba7-128">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="12ba7-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="12ba7-129">在“用户身份”字段，输入或选一个值。</span><span class="sxs-lookup"><span data-stu-id="12ba7-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="12ba7-130">选择“Alicia”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-130">Select Alicia.</span></span>  
8. <span data-ttu-id="12ba7-131">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="12ba7-132">在成本核算中启用访问权限</span><span class="sxs-lookup"><span data-stu-id="12ba7-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="12ba7-133">转至“成本核算”>“设置”>“参数”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="12ba7-134">单击“常规”选项卡。</span><span class="sxs-lookup"><span data-stu-id="12ba7-134">Click the General tab.</span></span>
3. <span data-ttu-id="12ba7-135">在“为成本对象维度成员启用视图访问”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="12ba7-136">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-136">Click Save.</span></span>
5. <span data-ttu-id="12ba7-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="12ba7-137">Close the page.</span></span>
6. <span data-ttu-id="12ba7-138">转至“成本核算”>“设置”>“成本控制工作区配置”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="12ba7-139">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-139">Click Edit.</span></span>
8. <span data-ttu-id="12ba7-140">在“已发布”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="12ba7-141">如果选择“是”，为其分配了以下四种角色之一的用户可查看“成本控制”工作区中的报表：成本核算经理、成本会计师、成本核算师和成本对象总监。</span><span class="sxs-lookup"><span data-stu-id="12ba7-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="12ba7-142">如果选择“否”，为其分配了以下角色之一的用户可查看报表：成本核算经理、成本会计师和成本核算师。</span><span class="sxs-lookup"><span data-stu-id="12ba7-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="12ba7-143">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="12ba7-143">Click Save.</span></span>

