---
title: 创建新用户
description: 用户是您的组织的内部员工或外部客户和供应商，该用户需要访问系统以履行职责。
author: maertenm
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a542ece226750330262e0c44427e5654fa4f6369
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916476"
---
# <a name="create-new-users"></a><span data-ttu-id="72b2b-103">创建新用户</span><span class="sxs-lookup"><span data-stu-id="72b2b-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="72b2b-104">用户是您的组织的内部员工或外部客户和供应商，该用户需要访问系统以履行职责。</span><span class="sxs-lookup"><span data-stu-id="72b2b-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="72b2b-105">系统管理员可以完成该过程，以将用户添加到系统。</span><span class="sxs-lookup"><span data-stu-id="72b2b-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="72b2b-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="72b2b-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="72b2b-107">添加新用户</span><span class="sxs-lookup"><span data-stu-id="72b2b-107">Add a new user</span></span>
1. <span data-ttu-id="72b2b-108">转到**导航窗格 > 模块 > 系统管理 > 用户 > 用户**。</span><span class="sxs-lookup"><span data-stu-id="72b2b-108">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="72b2b-109">在**操作窗格**中，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="72b2b-109">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="72b2b-110">在**用户 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="72b2b-110">In the **User ID** field, type a value.</span></span> <span data-ttu-id="72b2b-111">输入用户适用的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="72b2b-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="72b2b-112">用户 ID 是必填项。</span><span class="sxs-lookup"><span data-stu-id="72b2b-112">A user ID is required.</span></span>  
4. <span data-ttu-id="72b2b-113">在**用户名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="72b2b-113">In the **User name** field, type a value.</span></span> <span data-ttu-id="72b2b-114">输入用户的名称。</span><span class="sxs-lookup"><span data-stu-id="72b2b-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="72b2b-115">在**域**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="72b2b-115">In the **Domain** field, type a value.</span></span> <span data-ttu-id="72b2b-116">输入用户的域名。</span><span class="sxs-lookup"><span data-stu-id="72b2b-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="72b2b-117">在**别名**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="72b2b-117">In the **Alias** field, type a value.</span></span> <span data-ttu-id="72b2b-118">输入用户的别名。</span><span class="sxs-lookup"><span data-stu-id="72b2b-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="72b2b-119">在**公司**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="72b2b-119">In the **Company** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="72b2b-120">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="72b2b-120">In the list, find and select the desired record.</span></span> 
9. <span data-ttu-id="72b2b-121">在**用户的角色**部分中，单击**分配角色**。</span><span class="sxs-lookup"><span data-stu-id="72b2b-121">In the **User's roles** section, click **Assign roles**.</span></span>
10. <span data-ttu-id="72b2b-122">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="72b2b-122">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="72b2b-123">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="72b2b-123">Click **OK**.</span></span>
12. <span data-ttu-id="72b2b-124">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="72b2b-124">Click **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="72b2b-125">导入用户</span><span class="sxs-lookup"><span data-stu-id="72b2b-125">Import users</span></span>
1. <span data-ttu-id="72b2b-126">在**操作窗格**上，单击**导入用户**。</span><span class="sxs-lookup"><span data-stu-id="72b2b-126">On the **Action pane**, click **Import users**.</span></span>
2. <span data-ttu-id="72b2b-127">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="72b2b-127">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="72b2b-128">单击**导入用户**。</span><span class="sxs-lookup"><span data-stu-id="72b2b-128">Click **Import users**.</span></span>
4. <span data-ttu-id="72b2b-129">单击**关闭**。</span><span class="sxs-lookup"><span data-stu-id="72b2b-129">Click **Close**.</span></span>

