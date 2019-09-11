---
title: 创建 POS 权限组
description: 本主题介绍如何创建 POS 权限组。
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e6782c60aa659523775cc6c4eb1694430a4bf4f
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914774"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="5d445-103">创建 POS 权限组</span><span class="sxs-lookup"><span data-stu-id="5d445-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5d445-104">本主题介绍如何创建 POS 权限组。</span><span class="sxs-lookup"><span data-stu-id="5d445-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="5d445-105">创建此任务的演示数据公司是 USRT。</span><span class="sxs-lookup"><span data-stu-id="5d445-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="5d445-106">此任务旨在面向零售运营经理。</span><span class="sxs-lookup"><span data-stu-id="5d445-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="5d445-107">在导航窗格中，转到**模块 > Retail > 员工 > 权限组**。</span><span class="sxs-lookup"><span data-stu-id="5d445-107">In the navigation pane, go to **Modules > Retail > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="5d445-108">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="5d445-108">Select **New**.</span></span>
3. <span data-ttu-id="5d445-109">在 **POS 权限组 ID** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="5d445-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="5d445-110">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="5d445-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="5d445-111">选择**查看时钟条目**字段中的**是**。</span><span class="sxs-lookup"><span data-stu-id="5d445-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="5d445-112">您现在可以启用或禁用您的 POS 权限组的各种权限。</span><span class="sxs-lookup"><span data-stu-id="5d445-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="5d445-113">对于某些权限，您可以设置一个值，以用于评估 POS 用户是否可以执行该操作。</span><span class="sxs-lookup"><span data-stu-id="5d445-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="5d445-114">此任务指南会启用某些可能提供给出纳员的权限。</span><span class="sxs-lookup"><span data-stu-id="5d445-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="5d445-115">选择**允许创建订单**字段中的**是**。</span><span class="sxs-lookup"><span data-stu-id="5d445-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="5d445-116">选择**允许编辑订单**字段中的**是**。</span><span class="sxs-lookup"><span data-stu-id="5d445-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="5d445-117">选择**允许检索订单**字段中的**是**。</span><span class="sxs-lookup"><span data-stu-id="5d445-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="5d445-118">选择**允许密码更改**字段中的**是**。</span><span class="sxs-lookup"><span data-stu-id="5d445-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="5d445-119">选择**允许直接结束**字段中的**是**。</span><span class="sxs-lookup"><span data-stu-id="5d445-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="5d445-120">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="5d445-120">Select **Save**.</span></span> <span data-ttu-id="5d445-121">在您的更改保存之后，您需要运行“人员分配计划”，以将这些更改应用到零售渠道。</span><span class="sxs-lookup"><span data-stu-id="5d445-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span> 
12. <span data-ttu-id="5d445-122">在导航窗格中，转到**导航窗格 > 模块 > 人力资源 > 作业 > 作业**。</span><span class="sxs-lookup"><span data-stu-id="5d445-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="5d445-123">接下来，我们会将 POS 权限组分配到某一作业。</span><span class="sxs-lookup"><span data-stu-id="5d445-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="5d445-124">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="5d445-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="5d445-125">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="5d445-125">Select **Edit**.</span></span>
15. <span data-ttu-id="5d445-126">展开**工作分类**部分。</span><span class="sxs-lookup"><span data-stu-id="5d445-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="5d445-127">在“POS 权限组 ID”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5d445-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="5d445-128">除非工作人员 POS 权限已在其职位级别进行覆写，此作业所对应职位的所有工作人员都将使用此 POS 权限组的设置。</span><span class="sxs-lookup"><span data-stu-id="5d445-128">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="5d445-129">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="5d445-129">Select **Save**.</span></span> <span data-ttu-id="5d445-130">在您的更改保存之后，您需要运行“人员分配计划”，以将这些更改应用到零售渠道。</span><span class="sxs-lookup"><span data-stu-id="5d445-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  

