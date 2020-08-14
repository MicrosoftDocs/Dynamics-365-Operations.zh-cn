---
title: 创建和管理客户门户用户
description: 本主题说明如何创建客户门户用户帐户并为其设置权限。
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: c56e41b8ea5039531205083b5b42aff05e05cf66
ms.sourcegitcommit: 713b5dfc76a6875d0ba6d86c5cbd585ea502cf9d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "3413939"
---
# <a name="create-and-manage-customer-portal-users"></a><span data-ttu-id="9fe05-103">创建和管理客户门户用户</span><span class="sxs-lookup"><span data-stu-id="9fe05-103">Create and manage Customer portal users</span></span>

<span data-ttu-id="9fe05-104">在现成的实现中，用户无法自助注册使用客户门户创建的网站。</span><span class="sxs-lookup"><span data-stu-id="9fe05-104">In the out-of-box implementation, there is no way for users to self-register for websites that are created by using the Customer portal.</span></span> <span data-ttu-id="9fe05-105">要登录和使用网站，必须由管理员邀请用户。Microsoft 有意阻止了用户自助注册的能力。</span><span class="sxs-lookup"><span data-stu-id="9fe05-105">To sign in and use a website, users must be invited by the admin. Microsoft has intentionally blocked the ability of users to self-register.</span></span>

<span data-ttu-id="9fe05-106">必须先为用户创建联系人记录，该用户才可以使用网站。</span><span class="sxs-lookup"><span data-stu-id="9fe05-106">Before a user can use a website, a contact record must be created for that user.</span></span> <span data-ttu-id="9fe05-107">此记录指示用户属于哪个客户帐户和法人。</span><span class="sxs-lookup"><span data-stu-id="9fe05-107">This record indicates which customer account and legal entity the user belongs to.</span></span> <span data-ttu-id="9fe05-108">此信息对于确保用户可以创建和查看销售订单至关重要。</span><span class="sxs-lookup"><span data-stu-id="9fe05-108">This information is essential for ensuring that the user can create and view sales orders.</span></span>

<span data-ttu-id="9fe05-109">用户自助注册时，将自动为其创建联系人记录。</span><span class="sxs-lookup"><span data-stu-id="9fe05-109">When users self-register, contact records are automatically created for them.</span></span> <span data-ttu-id="9fe05-110">因此，您无法确保用户选择正确的客户帐户和法人。</span><span class="sxs-lookup"><span data-stu-id="9fe05-110">Therefore, you can't ensure that a user selects the correct customer account and legal entity.</span></span> <span data-ttu-id="9fe05-111">另一方面，邀请流程允许管理员在邀请发送之前将正确的客户帐户和法人分配给联系人记录。</span><span class="sxs-lookup"><span data-stu-id="9fe05-111">On the other hand, the invitation process lets an admin assign the correct customer account and legal entity to the contact record before an invitation is sent.</span></span> <span data-ttu-id="9fe05-112">如果您正在考虑自定义解决方案以使用户可以自助注册，请务必考虑可能的后果。</span><span class="sxs-lookup"><span data-stu-id="9fe05-112">If you're thinking about customizing the solution so that users can self-register, be sure to consider the possible consequences.</span></span>

## <a name="prerequisite-setup"></a><span data-ttu-id="9fe05-113">先决条件设置</span><span class="sxs-lookup"><span data-stu-id="9fe05-113">Prerequisite setup</span></span>

<span data-ttu-id="9fe05-114">Power Apps 门户中的联系人作为记录存储在 Common Data Service 中的**联系人**实体中。</span><span class="sxs-lookup"><span data-stu-id="9fe05-114">Contacts in Power Apps portals are stored as records in the **Contacts** entity in Common Data Service.</span></span> <span data-ttu-id="9fe05-115">然后双写入根据需要将这些记录同步到 Microsoft Dynamics 365 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="9fe05-115">Dual-write then syncs these records to Microsoft Dynamics 365 Supply Chain Management as required.</span></span>

![![客户门户联系人的系统图](media/customer-portal-contacts.png "客户门户联系人的系统图")](media/customer-portal-contacts.png "System diagram for Customer portal contacts")

<span data-ttu-id="9fe05-117">在开始邀请新客户之前，请确保以双写入形式启用了**联系人**实体映射。</span><span class="sxs-lookup"><span data-stu-id="9fe05-117">Before you start to invite new customers, make sure that you've enabled the **Contact** entity mapping in dual-write.</span></span>

## <a name="the-invitation-process"></a><span data-ttu-id="9fe05-118">邀请流程</span><span class="sxs-lookup"><span data-stu-id="9fe05-118">The invitation process</span></span>

<span data-ttu-id="9fe05-119">要将现有联系人邀请到客户门户，请按照 Power Apps 门户文档中的[向门户邀请联系人](https://docs.microsoft.com/powerapps/maker/portals/configure/invite-contacts)中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="9fe05-119">To invite an existing contact to the Customer portal, follow the steps in [Invite contacts to your portals](https://docs.microsoft.com/powerapps/maker/portals/configure/invite-contacts) in the Power Apps portals documentation.</span></span>

<span data-ttu-id="9fe05-120">在邀请客户加入客户门户之前，请确保客户的[联系人记录](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts)已通过以下方式提供并设置：</span><span class="sxs-lookup"><span data-stu-id="9fe05-120">Before you invite a customer to join the Customer portal, make sure that the customer's [contact record](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) is available and set up in the following way:</span></span>

1. <span data-ttu-id="9fe05-121">将**公司**字段设置为您希望客户在 Supply Chain Management 中所属的法人。</span><span class="sxs-lookup"><span data-stu-id="9fe05-121">Set the **Company** field to the legal entity that you want the customer to belong to in Supply Chain Management.</span></span>
2. <span data-ttu-id="9fe05-122">将**帐号**字段设置为您希望用户在 Supply Chain Management 中拥有的客户帐号。</span><span class="sxs-lookup"><span data-stu-id="9fe05-122">Set the **Account Number** field to the customer account number that you want the user to have in Supply Chain Management.</span></span>

<span data-ttu-id="9fe05-123">联系人创建后，您应该可以在 Supply Chain Management 中看到它。</span><span class="sxs-lookup"><span data-stu-id="9fe05-123">After a contact is created, you should be able to see it in Supply Chain Management.</span></span>

<span data-ttu-id="9fe05-124">有关详细信息，请参阅 Power Apps 门户文档中的[配置要在门户上使用的联系人](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts)。</span><span class="sxs-lookup"><span data-stu-id="9fe05-124">For more information, see [Configure a contact for use on a portal](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) in the Power Apps portals documentation.</span></span>

## <a name="out-of-box-web-roles-and-entity-permissions"></a><span data-ttu-id="9fe05-125">现成的 Web 角色和实体权限</span><span class="sxs-lookup"><span data-stu-id="9fe05-125">Out-of-box web roles and entity permissions</span></span>

<span data-ttu-id="9fe05-126">Power Apps 门户中的用户角色由 [Web 角色](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles)和[实体权限](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions)定义。</span><span class="sxs-lookup"><span data-stu-id="9fe05-126">User roles in Power Apps portals are defined by [web roles](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) and [entity permissions](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions).</span></span> <span data-ttu-id="9fe05-127">为客户门户定义了一些现成角色。</span><span class="sxs-lookup"><span data-stu-id="9fe05-127">A few roles are defined for the Customer portal out of the box.</span></span> <span data-ttu-id="9fe05-128">您可以创建新角色，并可以修改或删除现有角色。</span><span class="sxs-lookup"><span data-stu-id="9fe05-128">You can create new roles, and you can modify or remove existing roles.</span></span>

### <a name="out-of-box-web-roles"></a><span data-ttu-id="9fe05-129">现成的 Web 角色</span><span class="sxs-lookup"><span data-stu-id="9fe05-129">Out-of-box web roles</span></span>

<span data-ttu-id="9fe05-130">本节介绍随客户门户提供的 Web 角色。</span><span class="sxs-lookup"><span data-stu-id="9fe05-130">This section describes the web roles that are delivered with the Customer portal.</span></span>

<span data-ttu-id="9fe05-131">有关如何修改现成的用户角色的详细信息，请参阅 Power Apps 门户文档中的[为门户创建 Web 角色](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles)和[使用门户的实体权限添加基于记录的安全性](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions)。</span><span class="sxs-lookup"><span data-stu-id="9fe05-131">For more information about how to modify the out-of-box user roles, see [Create web roles for portals](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) and [Add record-based security by using entity permissions for portals](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions) in the Power Apps portals documentation.</span></span>

#### <a name="administrator"></a><span data-ttu-id="9fe05-132">管理员</span><span class="sxs-lookup"><span data-stu-id="9fe05-132">Administrator</span></span>

<span data-ttu-id="9fe05-133">管理员负责监管和维护网站。</span><span class="sxs-lookup"><span data-stu-id="9fe05-133">The administrator oversees and maintains the website.</span></span> <span data-ttu-id="9fe05-134">此人将预配和设置客户门户。</span><span class="sxs-lookup"><span data-stu-id="9fe05-134">This person will provision and set up the Customer portal.</span></span> <span data-ttu-id="9fe05-135">管理员维护门户的 IT 和安全性，并确保一切顺利进行。</span><span class="sxs-lookup"><span data-stu-id="9fe05-135">The administrator maintains the IT and security aspects of the portal, and makes sure that everything runs smoothly.</span></span> <span data-ttu-id="9fe05-136">管理员还可以通过添加新功能、创建新角色等来自定义和/或更改门户。</span><span class="sxs-lookup"><span data-stu-id="9fe05-136">The administrator might also customize and/or change the portal by adding new functionalities, creating new roles, and more.</span></span>

#### <a name="customer-representative"></a><span data-ttu-id="9fe05-137">客户代表</span><span class="sxs-lookup"><span data-stu-id="9fe05-137">Customer representative</span></span>

<span data-ttu-id="9fe05-138">客户代表为客户公司工作，负责管理公司下的订单。</span><span class="sxs-lookup"><span data-stu-id="9fe05-138">A customer representative works for a customer company and is responsible for managing the orders that the company places.</span></span> <span data-ttu-id="9fe05-139">客户代表可以查看已为公司下达的所有订单以及下达订单的用户。</span><span class="sxs-lookup"><span data-stu-id="9fe05-139">The customer representative can see all the orders that have been placed for the company and the users who placed them.</span></span> <span data-ttu-id="9fe05-140">此外，客户代表还可以查看有关整个客户的信息，以及哪些联系人可以代表该客户下订单。</span><span class="sxs-lookup"><span data-stu-id="9fe05-140">Additionally, the customer representative can see information about the overall account and which contacts can place orders on behalf of that account.</span></span>

#### <a name="authorized-users"></a><span data-ttu-id="9fe05-141">授权用户</span><span class="sxs-lookup"><span data-stu-id="9fe05-141">Authorized users</span></span>

<span data-ttu-id="9fe05-142">授权用户可以下订单和查看所下订单的状态。</span><span class="sxs-lookup"><span data-stu-id="9fe05-142">Authorized users can place orders and view the status of the orders that they have placed.</span></span> <span data-ttu-id="9fe05-143">但是，他们无法查看公司中其他用户所下订单的状态。</span><span class="sxs-lookup"><span data-stu-id="9fe05-143">However, they can't view the status of orders that other users in their company have placed.</span></span>

#### <a name="unauthorized-users"></a><span data-ttu-id="9fe05-144">未授权用户</span><span class="sxs-lookup"><span data-stu-id="9fe05-144">Unauthorized users</span></span>

<span data-ttu-id="9fe05-145">未授权用户无法查看任何数据。</span><span class="sxs-lookup"><span data-stu-id="9fe05-145">Unauthorized users can't view any data.</span></span> <span data-ttu-id="9fe05-146">他们只能查看公共信息，如条款和条件，以及有关运行客户门户的公司的详细信息。</span><span class="sxs-lookup"><span data-stu-id="9fe05-146">They can see only public information, such as terms and conditions, and details about the company that is running the Customer portal.</span></span>

#### <a name="example"></a><span data-ttu-id="9fe05-147">示例</span><span class="sxs-lookup"><span data-stu-id="9fe05-147">Example</span></span>

<span data-ttu-id="9fe05-148">下表显示了每个 Web 角色的用户可以在系统中查看的销售订单。</span><span class="sxs-lookup"><span data-stu-id="9fe05-148">The following table shows which sales orders the users in each web role can see in the system.</span></span>

| <span data-ttu-id="9fe05-149">销售订单</span><span class="sxs-lookup"><span data-stu-id="9fe05-149">Sales order</span></span> | <span data-ttu-id="9fe05-150">管理员</span><span class="sxs-lookup"><span data-stu-id="9fe05-150">Administrator</span></span> | <span data-ttu-id="9fe05-151">客户&nbsp;X 的客户代表</span><span class="sxs-lookup"><span data-stu-id="9fe05-151">Customer representative for customer&nbsp;X</span></span> | <span data-ttu-id="9fe05-152">授权用户：Jane</span><span class="sxs-lookup"><span data-stu-id="9fe05-152">Authorized user: Jane</span></span> | <span data-ttu-id="9fe05-153">授权用户：Sam</span><span class="sxs-lookup"><span data-stu-id="9fe05-153">Authorized user: Sam</span></span> | <span data-ttu-id="9fe05-154">未授权用户：May</span><span class="sxs-lookup"><span data-stu-id="9fe05-154">Unauthorized user: May</span></span> |
|---|---|---|---|---|---|
| <span data-ttu-id="9fe05-155">客户&nbsp;X 订货人：Jane&nbsp;</span><span class="sxs-lookup"><span data-stu-id="9fe05-155">Customer&nbsp;X Orderer:&nbsp;Jane</span></span> | <span data-ttu-id="9fe05-156">是</span><span class="sxs-lookup"><span data-stu-id="9fe05-156">Yes</span></span> | <span data-ttu-id="9fe05-157">是</span><span class="sxs-lookup"><span data-stu-id="9fe05-157">Yes</span></span> | <span data-ttu-id="9fe05-158">是</span><span class="sxs-lookup"><span data-stu-id="9fe05-158">Yes</span></span> | <span data-ttu-id="9fe05-159">无</span><span class="sxs-lookup"><span data-stu-id="9fe05-159">No</span></span> | <span data-ttu-id="9fe05-160">无</span><span class="sxs-lookup"><span data-stu-id="9fe05-160">No</span></span> |
| <span data-ttu-id="9fe05-161">客户&nbsp;X 订货人：Sam&nbsp;</span><span class="sxs-lookup"><span data-stu-id="9fe05-161">Customer&nbsp;X Orderer:&nbsp;Sam</span></span> | <span data-ttu-id="9fe05-162">是</span><span class="sxs-lookup"><span data-stu-id="9fe05-162">Yes</span></span> | <span data-ttu-id="9fe05-163">是</span><span class="sxs-lookup"><span data-stu-id="9fe05-163">Yes</span></span> | <span data-ttu-id="9fe05-164">无</span><span class="sxs-lookup"><span data-stu-id="9fe05-164">No</span></span> | <span data-ttu-id="9fe05-165">是</span><span class="sxs-lookup"><span data-stu-id="9fe05-165">Yes</span></span> | <span data-ttu-id="9fe05-166">无</span><span class="sxs-lookup"><span data-stu-id="9fe05-166">No</span></span> |
| <span data-ttu-id="9fe05-167">客户&nbsp;Y 订货人：May&nbsp;</span><span class="sxs-lookup"><span data-stu-id="9fe05-167">Customer&nbsp;Y Orderer:&nbsp;May</span></span> | <span data-ttu-id="9fe05-168">是</span><span class="sxs-lookup"><span data-stu-id="9fe05-168">Yes</span></span> | <span data-ttu-id="9fe05-169">无</span><span class="sxs-lookup"><span data-stu-id="9fe05-169">No</span></span> | <span data-ttu-id="9fe05-170">无</span><span class="sxs-lookup"><span data-stu-id="9fe05-170">No</span></span> | <span data-ttu-id="9fe05-171">无</span><span class="sxs-lookup"><span data-stu-id="9fe05-171">No</span></span> | <span data-ttu-id="9fe05-172">无</span><span class="sxs-lookup"><span data-stu-id="9fe05-172">No</span></span> |

> [!NOTE]
> <span data-ttu-id="9fe05-173">即使 Sam 和 Jane 都是为客户 X 工作的联系人，他们也只能查看他们自己下的订单，而看不到其他信息。</span><span class="sxs-lookup"><span data-stu-id="9fe05-173">Even though both Sam and Jane are contacts who work for customer X, they can see only the orders that they themselves have placed and nothing else.</span></span> <span data-ttu-id="9fe05-174">尽管 May 在系统中有一个订单，但由于她是未授权用户，因此她无法在客户门户中查看该订单。</span><span class="sxs-lookup"><span data-stu-id="9fe05-174">Although May has an order in the system, she can't see that order in the Customer portal, because she is an unauthorized user.</span></span> <span data-ttu-id="9fe05-175">（而且，她一定是通过客户门户以外的某个渠道下的订单。）</span><span class="sxs-lookup"><span data-stu-id="9fe05-175">(Additionally, she must have placed the order through some channel other than the Customer portal.)</span></span>