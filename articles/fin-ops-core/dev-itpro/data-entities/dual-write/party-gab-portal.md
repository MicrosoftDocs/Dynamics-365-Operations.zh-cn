---
title: 将 Power Portal 与当事方数据模型配合使用
description: 本主题介绍由于双重写入中的当事方数据模型对 Power Portal Web 角色的更改。
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833082"
---
# <a name="using-power-portal-with-the-party-data-model"></a><span data-ttu-id="944ec-103">将 Power Portal 与当事方数据模型配合使用</span><span class="sxs-lookup"><span data-stu-id="944ec-103">Using Power Portal with the Party data model</span></span>

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="944ec-104">双重写入应用程序业务流程解决方案版本 2.0.999.0 及更高版本包括对帐户和联系人表的当事方和全球通讯簿的数据模型更改。</span><span class="sxs-lookup"><span data-stu-id="944ec-104">The Dual-write application orchestration solution version 2.0.999.0 and later includes data model changes to party and global address book for the Account and Contact tables.</span></span> <span data-ttu-id="944ec-105">这些更改允许支持高级业务方案的多对多关系。</span><span class="sxs-lookup"><span data-stu-id="944ec-105">The changes allow many-to-many relationships that support advanced business scenarios.</span></span> <span data-ttu-id="944ec-106">这些更改不受门户 Web 角色支持，包括客户门户，在安装双重写入之前，这些角色是现成的或存在于您的环境中。</span><span class="sxs-lookup"><span data-stu-id="944ec-106">These changes are not supported by portal web roles, including the customer portal, that are shipped out-of-the-box or that existed in your environment before you installed dual-write.</span></span> <span data-ttu-id="944ec-107">为了使 Web 角色按预期工作，您需要使用新的数据模型创建新 Web 角色。</span><span class="sxs-lookup"><span data-stu-id="944ec-107">For the web roles to work as expected, you need to create new web roles using the new data model.</span></span> 

<span data-ttu-id="944ec-108">总而言之，表交互的方式已更改，但是客户门户中的表权限未更改。</span><span class="sxs-lookup"><span data-stu-id="944ec-108">In summary, the way the tables interact has changed, but the table permissions in the customer portal haven't changed.</span></span> <span data-ttu-id="944ec-109">本主题说明如何创建与新的高级数据模型一起使用的新 Web 角色。</span><span class="sxs-lookup"><span data-stu-id="944ec-109">This topic explains how to create new web roles that work with the new advanced data model.</span></span>

<span data-ttu-id="944ec-110">该图显示了 **没有** 当事方和全球通讯簿数据模型的表关系：</span><span class="sxs-lookup"><span data-stu-id="944ec-110">This diagram shows the table relationship **without** the party and global address book data model:</span></span>

   ![没有当事方模型](media/without-party-model.PNG)

<span data-ttu-id="944ec-112">该图显示了 **具有** 当事方和全球通讯簿数据模型的表关系：</span><span class="sxs-lookup"><span data-stu-id="944ec-112">This diagram shows the table relationship **with** the party and global address book data model:</span></span>

   ![具有当事方模型](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a><span data-ttu-id="944ec-114">创建新的表权限</span><span class="sxs-lookup"><span data-stu-id="944ec-114">Create a new table permission</span></span>

<span data-ttu-id="944ec-115">若要创建这些新的表权限，请按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="944ec-115">To create these new table permissions, follow these steps:</span></span>

1. <span data-ttu-id="944ec-116">登录到 [Power Apps](https://make.powerapps.com)，然后转到您的应用。</span><span class="sxs-lookup"><span data-stu-id="944ec-116">Sign in to [Power Apps](https://make.powerapps.com), and go to your apps.</span></span>
2. <span data-ttu-id="944ec-117">选择您的门户管理应用。</span><span class="sxs-lookup"><span data-stu-id="944ec-117">Select your Portal Management app.</span></span>
3. <span data-ttu-id="944ec-118">在侧边栏中，选择 **安全性 > 表权限**。</span><span class="sxs-lookup"><span data-stu-id="944ec-118">In the side bar, select **Security > Table permissions**.</span></span>

    <span data-ttu-id="944ec-119">您必须创建三个新权限：</span><span class="sxs-lookup"><span data-stu-id="944ec-119">You must create three new permissions:</span></span>

    + <span data-ttu-id="944ec-120">联系人与当事方的连接</span><span class="sxs-lookup"><span data-stu-id="944ec-120">Contact to Party connection</span></span>
    + <span data-ttu-id="944ec-121">当事方与帐户的连接</span><span class="sxs-lookup"><span data-stu-id="944ec-121">Party to Account connection</span></span>
    + <span data-ttu-id="944ec-122">帐户与订单的连接</span><span class="sxs-lookup"><span data-stu-id="944ec-122">Account to Order connection</span></span>

4. <span data-ttu-id="944ec-123">创建并保存联系人与当事方的连接的新权限，设置以下参数：</span><span class="sxs-lookup"><span data-stu-id="944ec-123">Create and save a new permission for the Contact to Party connection, setting these parameters:</span></span>

    + <span data-ttu-id="944ec-124">**名称**：当事方与帐户的连接（或您的选择）</span><span class="sxs-lookup"><span data-stu-id="944ec-124">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="944ec-125">**表名称**：msdyn_contactforparty</span><span class="sxs-lookup"><span data-stu-id="944ec-125">**Table Name**: msdyn_contactforparty</span></span>
    + <span data-ttu-id="944ec-126">**网站**：客户门户</span><span class="sxs-lookup"><span data-stu-id="944ec-126">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="944ec-127">**范围**：联系人</span><span class="sxs-lookup"><span data-stu-id="944ec-127">**Scope**: Contact</span></span>
    + <span data-ttu-id="944ec-128">**特权**：全选</span><span class="sxs-lookup"><span data-stu-id="944ec-128">**Privileges**: Select all</span></span>
    + <span data-ttu-id="944ec-129">**Web 角色**：经过身份验证的用户、客户代表（或您的选择）</span><span class="sxs-lookup"><span data-stu-id="944ec-129">**Web roles**: Authenticated Users, Customer Representative (or your choice)</span></span>

5. <span data-ttu-id="944ec-130">创建并保存当事方与帐户的连接的新权限，设置以下参数：</span><span class="sxs-lookup"><span data-stu-id="944ec-130">Create and save a new permission for the Party to Account connection, setting these parameters:</span></span>

    + <span data-ttu-id="944ec-131">**名称**：当事方与帐户的连接（或您的选择）</span><span class="sxs-lookup"><span data-stu-id="944ec-131">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="944ec-132">**表名称**：帐户</span><span class="sxs-lookup"><span data-stu-id="944ec-132">**Table Name**: account</span></span>
    + <span data-ttu-id="944ec-133">**网站**：客户门户</span><span class="sxs-lookup"><span data-stu-id="944ec-133">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="944ec-134">**范围**：父级</span><span class="sxs-lookup"><span data-stu-id="944ec-134">**Scope**: Parent</span></span>
    + <span data-ttu-id="944ec-135">**特权**：全选</span><span class="sxs-lookup"><span data-stu-id="944ec-135">**Privileges**: Select all</span></span>
    + <span data-ttu-id="944ec-136">**父表权限**：联系人与当事方的连接</span><span class="sxs-lookup"><span data-stu-id="944ec-136">**Parent Table Permission**: Contact to Party Connection</span></span>

6. <span data-ttu-id="944ec-137">创建并保存帐户与订单的连接的新权限，设置以下参数：</span><span class="sxs-lookup"><span data-stu-id="944ec-137">Create and save a new permission for the Account to Order connection, setting these parameters:</span></span>

    + <span data-ttu-id="944ec-138">**名称**：帐户与订单的连接（或您的选择）</span><span class="sxs-lookup"><span data-stu-id="944ec-138">**Name**: Account to Order Connection (or your choice)</span></span>
    + <span data-ttu-id="944ec-139">**标名称**：销售订单</span><span class="sxs-lookup"><span data-stu-id="944ec-139">**Table Name**: salesorder</span></span>
    + <span data-ttu-id="944ec-140">**网站**：客户门户</span><span class="sxs-lookup"><span data-stu-id="944ec-140">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="944ec-141">**范围**：父级</span><span class="sxs-lookup"><span data-stu-id="944ec-141">**Scope**: Parent</span></span>
    + <span data-ttu-id="944ec-142">**特权**：全选</span><span class="sxs-lookup"><span data-stu-id="944ec-142">**Privileges**: Select all</span></span>
    + <span data-ttu-id="944ec-143">**父表权限**：当事方与帐户的连接</span><span class="sxs-lookup"><span data-stu-id="944ec-143">**Parent Table Permission**: Party to Account Connection</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
