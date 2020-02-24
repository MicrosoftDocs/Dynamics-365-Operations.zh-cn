---
title: 管理电子商务用户和角色
description: 此主题介绍如何为用户授予 Microsoft Dynamics 365 Commerce 站点创作环境的访问权限。
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a1f9abae20d0f2e71790a3b27337338dc042b52
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003525"
---
# <a name="manage-e-commerce-users-and-roles"></a><span data-ttu-id="2af77-103">管理电子商务用户和角色</span><span class="sxs-lookup"><span data-stu-id="2af77-103">Manage e-Commerce users and roles</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2af77-104">此主题介绍如何为用户授予 Microsoft Dynamics 365 Commerce 站点创作环境的访问权限。</span><span class="sxs-lookup"><span data-stu-id="2af77-104">This topic explains how to grant users access to the authoring environment for your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="2af77-105">为了帮助控制用户访问和授予用户执行特定任务的权限，站点制作环境使用您在 Microsoft Azure Active Directory (Azure AD) 中创建的安全组。</span><span class="sxs-lookup"><span data-stu-id="2af77-105">To help control user access and grant users permission to perform specific tasks, the site authoring environment uses security groups that you create in Microsoft Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="2af77-106">您首先从 Azure AD 将新的或现有的安全组分配给创作环境中的每位角色。</span><span class="sxs-lookup"><span data-stu-id="2af77-106">You first assign a new or existing security group from Azure AD to each role in the authoring environment.</span></span> <span data-ttu-id="2af77-107">然后为单个用户授予权限或撤消其权限，方法是将这些用户添加到相应安全组，或从安全组删除这些用户。</span><span class="sxs-lookup"><span data-stu-id="2af77-107">You then grant or revoke permissions for individual users by either adding those users to an appropriate security group or removing them from a security group.</span></span>

## <a name="overview-of-roles-in-the-authoring-environment"></a><span data-ttu-id="2af77-108">创作环境中的角色概述</span><span class="sxs-lookup"><span data-stu-id="2af77-108">Overview of roles in the authoring environment</span></span>

<span data-ttu-id="2af77-109">Dynamics 365 for Commerce 创作环境支持以下角色。</span><span class="sxs-lookup"><span data-stu-id="2af77-109">The Dynamics 365 for Commerce authoring environment supports the following roles.</span></span>

| <span data-ttu-id="2af77-110">角色</span><span class="sxs-lookup"><span data-stu-id="2af77-110">Role</span></span>                 | <span data-ttu-id="2af77-111">说明</span><span class="sxs-lookup"><span data-stu-id="2af77-111">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="2af77-112">系统管理员</span><span class="sxs-lookup"><span data-stu-id="2af77-112">System Administrator</span></span> | <span data-ttu-id="2af77-113">具有此角色的用户拥有所有工具和所有评分和评价的所有权限。</span><span class="sxs-lookup"><span data-stu-id="2af77-113">Users who have this role have all privileges for all tools, and for all ratings and reviews.</span></span> <span data-ttu-id="2af77-114">还可以创建站点。</span><span class="sxs-lookup"><span data-stu-id="2af77-114">They can also create sites.</span></span> |
| <span data-ttu-id="2af77-115">管理员</span><span class="sxs-lookup"><span data-stu-id="2af77-115">Administrator</span></span>   | <span data-ttu-id="2af77-116">具有此角色的用户拥有特定站点结构中所有工具和 RnR 的所有权限。</span><span class="sxs-lookup"><span data-stu-id="2af77-116">Users who have this role have all privileges for all tools and RnR in a given site structure.</span></span> |
| <span data-ttu-id="2af77-117">Web 制作者</span><span class="sxs-lookup"><span data-stu-id="2af77-117">Web Producer</span></span>         | <span data-ttu-id="2af77-118">具有此角色的用户可以创建页面、片段和模板，上传和管理资产，以及扩充产品和类别。</span><span class="sxs-lookup"><span data-stu-id="2af77-118">Users who have this role can create pages, fragments and templates, upload and manage assets, and enrich products and categories.</span></span> |
| <span data-ttu-id="2af77-119">读者</span><span class="sxs-lookup"><span data-stu-id="2af77-119">Reader</span></span>               | <span data-ttu-id="2af77-120">具有此角色的用户可查看页面、模板、资产、片段、布局和设置，但是不能进行更改。</span><span class="sxs-lookup"><span data-stu-id="2af77-120">Users who have this role can view pages, templates, assets, fragments, layouts and settings, but may not make changes.</span></span> |
| <span data-ttu-id="2af77-121">RnR 审查者</span><span class="sxs-lookup"><span data-stu-id="2af77-121">RnR Moderator</span></span>        | <span data-ttu-id="2af77-122">具有此角色的用户可以审查产品评价。</span><span class="sxs-lookup"><span data-stu-id="2af77-122">Users who have this role can moderate product reviews.</span></span> |

## <a name="system-administrator-role"></a><span data-ttu-id="2af77-123">系统管理员角色</span><span class="sxs-lookup"><span data-stu-id="2af77-123">System Administrator role</span></span>

<span data-ttu-id="2af77-124">在 Microsoft Dynamics Lifecycle Services (LCS) 环境中预配 Dynamics 365 Commerce 时，系统会请您为**系统管理员**角色提供安全组。</span><span class="sxs-lookup"><span data-stu-id="2af77-124">When you provision Dynamics 365 Commerce in the Microsoft Dynamics Lifecycle Services (LCS) environment, you're asked to provide a security group for the **System Administrator** role.</span></span> <span data-ttu-id="2af77-125">然后将此角色自动应用于您在正在配置的环境中创建的所有站点。</span><span class="sxs-lookup"><span data-stu-id="2af77-125">This role is then automatically applied to all sites that you create in the environment that you're configuring.</span></span> <span data-ttu-id="2af77-126">只能在 LCS 中更新此角色的安全组。</span><span class="sxs-lookup"><span data-stu-id="2af77-126">The security group for this role can be updated only in LCS.</span></span> <span data-ttu-id="2af77-127">在所有站点的**站点管理**页中，其显示为只读，仅供参考。</span><span class="sxs-lookup"><span data-stu-id="2af77-127">On the **Site Administration** page for all sites, it appears as read-only and is for informational purposes only.</span></span>

## <a name="administrator-role"></a><span data-ttu-id="2af77-128">管理员角色</span><span class="sxs-lookup"><span data-stu-id="2af77-128">Administrator role</span></span>

<span data-ttu-id="2af77-129">在 Commerce 中创建新站点时，系统将请您为**管理员**角色提供安全组。</span><span class="sxs-lookup"><span data-stu-id="2af77-129">When you create a new site in Commerce, you're asked to provide a security group for the **Administrator** role.</span></span> <span data-ttu-id="2af77-130">有关此角色授予的权限的概述，请参见本主题前文的表。</span><span class="sxs-lookup"><span data-stu-id="2af77-130">See the table earlier in this topic for an overview of the permissions that this role grants.</span></span>

## <a name="add-or-update-security-groups"></a><span data-ttu-id="2af77-131">添加或更新安全组</span><span class="sxs-lookup"><span data-stu-id="2af77-131">Add or update security groups</span></span>

<span data-ttu-id="2af77-132">创建站点之后，只有与**系统管理员**和**管理员**角色关联的安全组中的用户才能访问该站点的创作环境。</span><span class="sxs-lookup"><span data-stu-id="2af77-132">After your site is created, only users who are in the security groups that are associated with the **System Administrator** and **Administrator** roles can access the authoring environment for that site.</span></span> <span data-ttu-id="2af77-133">若要为 **Web 制作者**、**RnR 审查者**和**读者**角色分配用户，必须为这些角色分配安全组。</span><span class="sxs-lookup"><span data-stu-id="2af77-133">To assign users to the **Web Producer**, **RnR Moderator**, and **Reader** roles, you must assign security groups to those roles.</span></span> <span data-ttu-id="2af77-134">若要向角色添加安全组或更新当前分配给角色的安全组，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2af77-134">To add a security group to a role, or to update a security group that is currently assigned to a role, follow these steps.</span></span>

1. <span data-ttu-id="2af77-135">转到要更新的站点。</span><span class="sxs-lookup"><span data-stu-id="2af77-135">Go to the site that you want to update.</span></span>
1. <span data-ttu-id="2af77-136">在**站点管理**中，打开**安全**页。</span><span class="sxs-lookup"><span data-stu-id="2af77-136">In **Site management**, open the **Security** page.</span></span>
1. <span data-ttu-id="2af77-137">选择要修改的角色。</span><span class="sxs-lookup"><span data-stu-id="2af77-137">Select the role to modify.</span></span>
1. <span data-ttu-id="2af77-138">向角色添加安全组，或从角色中删除安全组。</span><span class="sxs-lookup"><span data-stu-id="2af77-138">Add security groups to roles, or remove security groups from roles.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2af77-139">其他资源</span><span class="sxs-lookup"><span data-stu-id="2af77-139">Additional resources</span></span>

[<span data-ttu-id="2af77-140">将脚本代码添加到站点页面以支持遥测</span><span class="sxs-lookup"><span data-stu-id="2af77-140">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="2af77-141">站点的搜索引擎优化 (SEO) 注意事项</span><span class="sxs-lookup"><span data-stu-id="2af77-141">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)

[<span data-ttu-id="2af77-142">管理内容安全策略 (CSP)</span><span class="sxs-lookup"><span data-stu-id="2af77-142">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
