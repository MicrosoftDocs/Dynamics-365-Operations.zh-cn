---
title: 分配租赁用户角色
description: 本主题描述资产租赁中使用的安全角色。 它还说明了如何将用户分配给这些角色。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b31d0880d4f2cd2b8ad2dffcfe279421f935ed35
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440962"
---
# <a name="assign-lease-user-roles"></a><span data-ttu-id="6e53d-104">分配租赁用户角色</span><span class="sxs-lookup"><span data-stu-id="6e53d-104">Assign lease user roles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e53d-105">本主题描述资产租赁中使用的安全角色。</span><span class="sxs-lookup"><span data-stu-id="6e53d-105">This topic describes the security roles that are used in Asset leasing.</span></span> <span data-ttu-id="6e53d-106">它还说明了如何将用户分配给这些角色。</span><span class="sxs-lookup"><span data-stu-id="6e53d-106">It also explains how to assign users to those roles.</span></span>

<span data-ttu-id="6e53d-107">三个用户角色区分资产租赁中的访问权限。</span><span class="sxs-lookup"><span data-stu-id="6e53d-107">Three user roles differentiate access in Asset leasing.</span></span> <span data-ttu-id="6e53d-108">一种角色适合于维护租赁，一种角色适合于查看租赁，而另一种角色适合于履行租赁业务员的职责。</span><span class="sxs-lookup"><span data-stu-id="6e53d-108">One role is appropriate for maintaining leases, one is appropriate for viewing leases, and one is appropriate for performing a lease clerk's duties.</span></span> <span data-ttu-id="6e53d-109">每个角色有所有租赁页面的特定权限，并且每个角色都允许用户根据其工作职责查看，创建，编辑或删除租赁。</span><span class="sxs-lookup"><span data-stu-id="6e53d-109">Each role has specific permissions for all lease pages, and each lets users view, create, edit, or delete leases, according to their job duties.</span></span>

| <span data-ttu-id="6e53d-110">角色</span><span class="sxs-lookup"><span data-stu-id="6e53d-110">Role</span></span>           | <span data-ttu-id="6e53d-111">说明</span><span class="sxs-lookup"><span data-stu-id="6e53d-111">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="6e53d-112">维护租赁</span><span class="sxs-lookup"><span data-stu-id="6e53d-112">Maintain Lease</span></span> | <span data-ttu-id="6e53d-113">此角色的用户可以添加，编辑，删除和查看租赁。</span><span class="sxs-lookup"><span data-stu-id="6e53d-113">Users in this role can add, edit, delete, and view leases.</span></span> <span data-ttu-id="6e53d-114">该角色是为日常用户设计的，这些用户的任务包括创建和发布月度日记帐条目和添加新租赁。</span><span class="sxs-lookup"><span data-stu-id="6e53d-114">This role is designed for daily users whose tasks include creating and posting monthly journal entries and adding new leases.</span></span> <span data-ttu-id="6e53d-115">此角色提供所有资产租赁功能的访问权限。</span><span class="sxs-lookup"><span data-stu-id="6e53d-115">This role gives access to all Asset leasing functionality.</span></span> |
| <span data-ttu-id="6e53d-116">查看租赁</span><span class="sxs-lookup"><span data-stu-id="6e53d-116">View Lease</span></span>     | <span data-ttu-id="6e53d-117">此角色的用户只能查看租赁记录，计划和运行报告。</span><span class="sxs-lookup"><span data-stu-id="6e53d-117">Users in this role can only view lease records, schedules, and run reports.</span></span> <span data-ttu-id="6e53d-118">不能创建新租赁，编辑现有租赁或根据租赁创建日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="6e53d-118">They can't create new leases, edit existing leases, or create journal entries against leases.</span></span> <span data-ttu-id="6e53d-119">该角色是为只需要查看租赁，租赁计划以及针对这些租赁发生的交易的用户设计的。</span><span class="sxs-lookup"><span data-stu-id="6e53d-119">The role is designed for users who just have to view leases, lease schedules, and the transactions that occur against those leases.</span></span> |
| <span data-ttu-id="6e53d-120">租赁业务员</span><span class="sxs-lookup"><span data-stu-id="6e53d-120">Lease Clerk</span></span>    | <span data-ttu-id="6e53d-121">此角色的用户只能创建新租赁。</span><span class="sxs-lookup"><span data-stu-id="6e53d-121">Users in this role can only create new leases.</span></span> <span data-ttu-id="6e53d-122">不能编辑或删除现有租赁，查看租赁计划或过帐租赁日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="6e53d-122">They can't edit or delete existing leases, view lease schedules, or post leasing journal entries.</span></span> <span data-ttu-id="6e53d-123">该角色是为执行数据输入功能的用户设计的。</span><span class="sxs-lookup"><span data-stu-id="6e53d-123">This role is designed for users who work in a data entry capacity.</span></span> |

<span data-ttu-id="6e53d-124">请按照以下步骤将用户分配给资产租赁中使用的角色。</span><span class="sxs-lookup"><span data-stu-id="6e53d-124">Follow these steps to assign users to the roles that are used in Asset leasing.</span></span>

1. <span data-ttu-id="6e53d-125">转到 **系统管理 \> 安全 \> 将用户分配到角色**。</span><span class="sxs-lookup"><span data-stu-id="6e53d-125">Go to **System administration \> Security \> Assign users to roles**.</span></span>
2. <span data-ttu-id="6e53d-126">选择 **维护租赁**、**租赁业务员** 或 **查看租赁** 角色，然后选择 **手动分配/排除用户**。</span><span class="sxs-lookup"><span data-stu-id="6e53d-126">Select the **Maintain lease**, **Lease clerk**, or **View lease** role, and then select **Manually assign/exclude users**.</span></span>
3. <span data-ttu-id="6e53d-127">选择要分配给该角色的用户，然后选择 **分配给角色**。</span><span class="sxs-lookup"><span data-stu-id="6e53d-127">Select the user to assign to the role, and then select **Assign to role**.</span></span>
