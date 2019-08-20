---
title: 创建新用户
description: 用户是您的组织的内部员工或外部客户和供应商，该用户需要访问系统以履行职责。
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 89e492ef5030dd28020094152259b615010aa676
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851303"
---
# <a name="create-new-users"></a><span data-ttu-id="45d50-103">创建新用户</span><span class="sxs-lookup"><span data-stu-id="45d50-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="45d50-104">用户是您的组织的内部员工或外部客户和供应商，该用户需要访问系统以履行职责。</span><span class="sxs-lookup"><span data-stu-id="45d50-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="45d50-105">系统管理员可以完成该过程，以将用户添加到系统。</span><span class="sxs-lookup"><span data-stu-id="45d50-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="45d50-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="45d50-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="45d50-107">添加新用户</span><span class="sxs-lookup"><span data-stu-id="45d50-107">Add a new user</span></span>
1. <span data-ttu-id="45d50-108">转到“系统管理”>“用户”>“用户”。</span><span class="sxs-lookup"><span data-stu-id="45d50-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="45d50-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="45d50-109">Click New.</span></span>
3. <span data-ttu-id="45d50-110">在“用户 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="45d50-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="45d50-111">输入用户适用的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="45d50-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="45d50-112">用户 ID 是必填项。</span><span class="sxs-lookup"><span data-stu-id="45d50-112">A user ID is required.</span></span>  
4. <span data-ttu-id="45d50-113">在“用户名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="45d50-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="45d50-114">输入用户的名称。</span><span class="sxs-lookup"><span data-stu-id="45d50-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="45d50-115">在“域名”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="45d50-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="45d50-116">输入用户的域名。</span><span class="sxs-lookup"><span data-stu-id="45d50-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="45d50-117">在“别名”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="45d50-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="45d50-118">输入用户的别名。</span><span class="sxs-lookup"><span data-stu-id="45d50-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="45d50-119">在“公司”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="45d50-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="45d50-120">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="45d50-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="45d50-121">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="45d50-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="45d50-122">选择用户的公司</span><span class="sxs-lookup"><span data-stu-id="45d50-122">Select the user's company</span></span>  
10. <span data-ttu-id="45d50-123">单击“分配角色”。</span><span class="sxs-lookup"><span data-stu-id="45d50-123">Click Assign roles.</span></span>
11. <span data-ttu-id="45d50-124">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="45d50-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="45d50-125">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="45d50-125">Click OK.</span></span>
13. <span data-ttu-id="45d50-126">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="45d50-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="45d50-127">导入用户</span><span class="sxs-lookup"><span data-stu-id="45d50-127">Import users</span></span>
1. <span data-ttu-id="45d50-128">单击“导入用户”。</span><span class="sxs-lookup"><span data-stu-id="45d50-128">Click Import users.</span></span>
2. <span data-ttu-id="45d50-129">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="45d50-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="45d50-130">单击“导入用户”。</span><span class="sxs-lookup"><span data-stu-id="45d50-130">Click Import users.</span></span>
4. <span data-ttu-id="45d50-131">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="45d50-131">Click Close.</span></span>

