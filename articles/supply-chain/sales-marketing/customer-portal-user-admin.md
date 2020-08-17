---
title: 创建和管理客户门户用户
description: 本主题说明如何创建客户门户用户帐户并为其设置权限。
author: dasani-madipalli
manager: tfehr
ms.date: 07/31/2020
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
ms.openlocfilehash: a751cbffd98b8d47ca7dad222f0ce374381a393d
ms.sourcegitcommit: 074fe7e77feb795148c3daf2e6ccbb8a88679343
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/31/2020
ms.locfileid: "3645305"
---
# <a name="create-and-manage-customer-portal-users"></a><span data-ttu-id="38b08-103">创建和管理客户门户用户</span><span class="sxs-lookup"><span data-stu-id="38b08-103">Create and manage Customer portal users</span></span>

<span data-ttu-id="38b08-104">在现成的实现中，用户无法自助注册使用客户门户创建的网站。</span><span class="sxs-lookup"><span data-stu-id="38b08-104">In the out-of-box implementation, there is no way for users to self-register for websites that are created by using the Customer portal.</span></span> <span data-ttu-id="38b08-105">要登录和使用网站，必须由管理员邀请用户。Microsoft 有意阻止了用户自助注册的能力。</span><span class="sxs-lookup"><span data-stu-id="38b08-105">To sign in and use a website, users must be invited by the admin. Microsoft has intentionally blocked the ability of users to self-register.</span></span>

<span data-ttu-id="38b08-106">必须先为用户创建联系人记录，该用户才可以使用网站。</span><span class="sxs-lookup"><span data-stu-id="38b08-106">Before a user can use a website, a contact record must be created for that user.</span></span> <span data-ttu-id="38b08-107">此记录指示用户属于哪个客户帐户和法人。</span><span class="sxs-lookup"><span data-stu-id="38b08-107">This record indicates which customer account and legal entity the user belongs to.</span></span> <span data-ttu-id="38b08-108">此信息对于确保用户可以创建和查看销售订单至关重要。</span><span class="sxs-lookup"><span data-stu-id="38b08-108">This information is essential for ensuring that the user can create and view sales orders.</span></span>

<span data-ttu-id="38b08-109">用户自助注册时，将自动为其创建联系人记录。</span><span class="sxs-lookup"><span data-stu-id="38b08-109">When users self-register, contact records are automatically created for them.</span></span> <span data-ttu-id="38b08-110">因此，您无法确保用户选择正确的客户帐户和法人。</span><span class="sxs-lookup"><span data-stu-id="38b08-110">Therefore, you can't ensure that a user selects the correct customer account and legal entity.</span></span> <span data-ttu-id="38b08-111">另一方面，邀请流程允许管理员在邀请发送之前将正确的客户帐户和法人分配给联系人记录。</span><span class="sxs-lookup"><span data-stu-id="38b08-111">On the other hand, the invitation process lets an admin assign the correct customer account and legal entity to the contact record before an invitation is sent.</span></span> <span data-ttu-id="38b08-112">如果您正在考虑自定义解决方案以使用户可以自助注册，请务必考虑可能的后果。</span><span class="sxs-lookup"><span data-stu-id="38b08-112">If you're thinking about customizing the solution so that users can self-register, be sure to consider the possible consequences.</span></span>

## <a name="video"></a><span data-ttu-id="38b08-113">视频</span><span class="sxs-lookup"><span data-stu-id="38b08-113">Video</span></span>
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ADkI]

<span data-ttu-id="38b08-114">[邀请客户注册和使用您的客户门户](https://youtu.be/drGUYHX9QIQ)视频（上方所示）包括在 YouTube 上提供的 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中。</span><span class="sxs-lookup"><span data-stu-id="38b08-114">The [Invite customers to register and use your customer portal](https://youtu.be/drGUYHX9QIQ) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="prerequisite-setup"></a><span data-ttu-id="38b08-115">先决条件设置</span><span class="sxs-lookup"><span data-stu-id="38b08-115">Prerequisite setup</span></span>

<span data-ttu-id="38b08-116">Power Apps 门户中的联系人作为记录存储在 Common Data Service 中的**联系人**实体中。</span><span class="sxs-lookup"><span data-stu-id="38b08-116">Contacts in Power Apps portals are stored as records in the **Contacts** entity in Common Data Service.</span></span> <span data-ttu-id="38b08-117">然后双写入根据需要将这些记录同步到 Microsoft Dynamics 365 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="38b08-117">Dual-write then syncs these records to Microsoft Dynamics 365 Supply Chain Management as required.</span></span>

<span data-ttu-id="38b08-118">![客户门户联系人的系统图](media/customer-portal-contacts.png "客户门户联系人的系统图")</span><span class="sxs-lookup"><span data-stu-id="38b08-118">![System diagram for Customer portal contacts](media/customer-portal-contacts.png "System diagram for Customer portal contacts")</span></span>

<span data-ttu-id="38b08-119">在开始邀请新客户之前，请确保以双写入形式启用了**联系人**实体映射。</span><span class="sxs-lookup"><span data-stu-id="38b08-119">Before you start to invite new customers, make sure that you've enabled the **Contact** entity mapping in dual-write.</span></span>

## <a name="the-invitation-process"></a><span data-ttu-id="38b08-120">邀请流程</span><span class="sxs-lookup"><span data-stu-id="38b08-120">The invitation process</span></span>

<span data-ttu-id="38b08-121">要将现有联系人邀请到客户门户，请按照 Power Apps 门户文档中的[向门户邀请联系人](https://docs.microsoft.com/powerapps/maker/portals/configure/invite-contacts)中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="38b08-121">To invite an existing contact to the Customer portal, follow the steps in [Invite contacts to your portals](https://docs.microsoft.com/powerapps/maker/portals/configure/invite-contacts) in the Power Apps portals documentation.</span></span>

<span data-ttu-id="38b08-122">在邀请客户加入客户门户之前，请确保客户的[联系人记录](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts)已通过以下方式提供并设置：</span><span class="sxs-lookup"><span data-stu-id="38b08-122">Before you invite a customer to join the Customer portal, make sure that the customer's [contact record](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) is available and set up in the following way:</span></span>

1. <span data-ttu-id="38b08-123">将**公司**字段设置为您希望客户在 Supply Chain Management 中所属的法人。</span><span class="sxs-lookup"><span data-stu-id="38b08-123">Set the **Company** field to the legal entity that you want the customer to belong to in Supply Chain Management.</span></span>
2. <span data-ttu-id="38b08-124">将**帐号**字段设置为您希望用户在 Supply Chain Management 中拥有的客户帐号。</span><span class="sxs-lookup"><span data-stu-id="38b08-124">Set the **Account Number** field to the customer account number that you want the user to have in Supply Chain Management.</span></span>

<span data-ttu-id="38b08-125">联系人创建后，您应该可以在 Supply Chain Management 中看到它。</span><span class="sxs-lookup"><span data-stu-id="38b08-125">After a contact is created, you should be able to see it in Supply Chain Management.</span></span>

<span data-ttu-id="38b08-126">有关详细信息，请参阅 Power Apps 门户文档中的[配置要在门户上使用的联系人](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts)。</span><span class="sxs-lookup"><span data-stu-id="38b08-126">For more information, see [Configure a contact for use on a portal](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) in the Power Apps portals documentation.</span></span>

## <a name="out-of-box-web-roles-and-entity-permissions"></a><span data-ttu-id="38b08-127">现成的 Web 角色和实体权限</span><span class="sxs-lookup"><span data-stu-id="38b08-127">Out-of-box web roles and entity permissions</span></span>

<span data-ttu-id="38b08-128">Power Apps 门户中的用户角色由 [Web 角色](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles)和[实体权限](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions)定义。</span><span class="sxs-lookup"><span data-stu-id="38b08-128">User roles in Power Apps portals are defined by [web roles](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) and [entity permissions](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions).</span></span> <span data-ttu-id="38b08-129">为客户门户定义了一些现成角色。</span><span class="sxs-lookup"><span data-stu-id="38b08-129">A few roles are defined for the Customer portal out of the box.</span></span> <span data-ttu-id="38b08-130">您可以创建新角色，并可以修改或删除现有角色。</span><span class="sxs-lookup"><span data-stu-id="38b08-130">You can create new roles, and you can modify or remove existing roles.</span></span>

### <a name="out-of-box-web-roles"></a><span data-ttu-id="38b08-131">现成的 Web 角色</span><span class="sxs-lookup"><span data-stu-id="38b08-131">Out-of-box web roles</span></span>

<span data-ttu-id="38b08-132">本节介绍随客户门户提供的 Web 角色。</span><span class="sxs-lookup"><span data-stu-id="38b08-132">This section describes the web roles that are delivered with the Customer portal.</span></span>

<span data-ttu-id="38b08-133">有关如何修改现成的用户角色的详细信息，请参阅 Power Apps 门户文档中的[为门户创建 Web 角色](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles)和[使用门户的实体权限添加基于记录的安全性](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions)。</span><span class="sxs-lookup"><span data-stu-id="38b08-133">For more information about how to modify the out-of-box user roles, see [Create web roles for portals](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) and [Add record-based security by using entity permissions for portals](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions) in the Power Apps portals documentation.</span></span>

#### <a name="administrator"></a><span data-ttu-id="38b08-134">管理员</span><span class="sxs-lookup"><span data-stu-id="38b08-134">Administrator</span></span>

<span data-ttu-id="38b08-135">管理员负责监管和维护网站。</span><span class="sxs-lookup"><span data-stu-id="38b08-135">The administrator oversees and maintains the website.</span></span> <span data-ttu-id="38b08-136">此人将预配和设置客户门户。</span><span class="sxs-lookup"><span data-stu-id="38b08-136">This person will provision and set up the Customer portal.</span></span> <span data-ttu-id="38b08-137">管理员维护门户的 IT 和安全性，并确保一切顺利进行。</span><span class="sxs-lookup"><span data-stu-id="38b08-137">The administrator maintains the IT and security aspects of the portal, and makes sure that everything runs smoothly.</span></span> <span data-ttu-id="38b08-138">管理员还可以通过添加新功能、创建新角色等来自定义和/或更改门户。</span><span class="sxs-lookup"><span data-stu-id="38b08-138">The administrator might also customize and/or change the portal by adding new functionalities, creating new roles, and more.</span></span>

#### <a name="customer-representative"></a><span data-ttu-id="38b08-139">客户代表</span><span class="sxs-lookup"><span data-stu-id="38b08-139">Customer representative</span></span>

<span data-ttu-id="38b08-140">客户代表为客户公司工作，负责管理公司下的订单。</span><span class="sxs-lookup"><span data-stu-id="38b08-140">A customer representative works for a customer company and is responsible for managing the orders that the company places.</span></span> <span data-ttu-id="38b08-141">客户代表可以查看已为公司下达的所有订单以及下达订单的用户。</span><span class="sxs-lookup"><span data-stu-id="38b08-141">The customer representative can see all the orders that have been placed for the company and the users who placed them.</span></span> <span data-ttu-id="38b08-142">此外，客户代表还可以查看有关整个客户的信息，以及哪些联系人可以代表该客户下订单。</span><span class="sxs-lookup"><span data-stu-id="38b08-142">Additionally, the customer representative can see information about the overall account and which contacts can place orders on behalf of that account.</span></span>

#### <a name="authorized-users"></a><span data-ttu-id="38b08-143">授权用户</span><span class="sxs-lookup"><span data-stu-id="38b08-143">Authorized users</span></span>

<span data-ttu-id="38b08-144">授权用户可以下订单和查看所下订单的状态。</span><span class="sxs-lookup"><span data-stu-id="38b08-144">Authorized users can place orders and view the status of the orders that they have placed.</span></span> <span data-ttu-id="38b08-145">但是，他们无法查看公司中其他用户所下订单的状态。</span><span class="sxs-lookup"><span data-stu-id="38b08-145">However, they can't view the status of orders that other users in their company have placed.</span></span>

#### <a name="unauthorized-users"></a><span data-ttu-id="38b08-146">未授权用户</span><span class="sxs-lookup"><span data-stu-id="38b08-146">Unauthorized users</span></span>

<span data-ttu-id="38b08-147">未授权用户无法查看任何数据。</span><span class="sxs-lookup"><span data-stu-id="38b08-147">Unauthorized users can't view any data.</span></span> <span data-ttu-id="38b08-148">他们只能查看公共信息，如条款和条件，以及有关运行客户门户的公司的详细信息。</span><span class="sxs-lookup"><span data-stu-id="38b08-148">They can see only public information, such as terms and conditions, and details about the company that is running the Customer portal.</span></span>

#### <a name="example"></a><span data-ttu-id="38b08-149">示例</span><span class="sxs-lookup"><span data-stu-id="38b08-149">Example</span></span>

<span data-ttu-id="38b08-150">下表显示了每个 Web 角色的用户可以在系统中查看的销售订单。</span><span class="sxs-lookup"><span data-stu-id="38b08-150">The following table shows which sales orders the users in each web role can see in the system.</span></span>

| <span data-ttu-id="38b08-151">销售订单</span><span class="sxs-lookup"><span data-stu-id="38b08-151">Sales order</span></span> | <span data-ttu-id="38b08-152">管理员</span><span class="sxs-lookup"><span data-stu-id="38b08-152">Administrator</span></span> | <span data-ttu-id="38b08-153">客户&nbsp;X 的客户代表</span><span class="sxs-lookup"><span data-stu-id="38b08-153">Customer representative for customer&nbsp;X</span></span> | <span data-ttu-id="38b08-154">授权用户：Jane</span><span class="sxs-lookup"><span data-stu-id="38b08-154">Authorized user: Jane</span></span> | <span data-ttu-id="38b08-155">授权用户：Sam</span><span class="sxs-lookup"><span data-stu-id="38b08-155">Authorized user: Sam</span></span> | <span data-ttu-id="38b08-156">未授权用户：May</span><span class="sxs-lookup"><span data-stu-id="38b08-156">Unauthorized user: May</span></span> |
|---|---|---|---|---|---|
| <span data-ttu-id="38b08-157">客户&nbsp;X 订货人：Jane&nbsp;</span><span class="sxs-lookup"><span data-stu-id="38b08-157">Customer&nbsp;X Orderer:&nbsp;Jane</span></span> | <span data-ttu-id="38b08-158">是</span><span class="sxs-lookup"><span data-stu-id="38b08-158">Yes</span></span> | <span data-ttu-id="38b08-159">是</span><span class="sxs-lookup"><span data-stu-id="38b08-159">Yes</span></span> | <span data-ttu-id="38b08-160">是</span><span class="sxs-lookup"><span data-stu-id="38b08-160">Yes</span></span> | <span data-ttu-id="38b08-161">无</span><span class="sxs-lookup"><span data-stu-id="38b08-161">No</span></span> | <span data-ttu-id="38b08-162">无</span><span class="sxs-lookup"><span data-stu-id="38b08-162">No</span></span> |
| <span data-ttu-id="38b08-163">客户&nbsp;X 订货人：Sam&nbsp;</span><span class="sxs-lookup"><span data-stu-id="38b08-163">Customer&nbsp;X Orderer:&nbsp;Sam</span></span> | <span data-ttu-id="38b08-164">是</span><span class="sxs-lookup"><span data-stu-id="38b08-164">Yes</span></span> | <span data-ttu-id="38b08-165">是</span><span class="sxs-lookup"><span data-stu-id="38b08-165">Yes</span></span> | <span data-ttu-id="38b08-166">无</span><span class="sxs-lookup"><span data-stu-id="38b08-166">No</span></span> | <span data-ttu-id="38b08-167">是</span><span class="sxs-lookup"><span data-stu-id="38b08-167">Yes</span></span> | <span data-ttu-id="38b08-168">无</span><span class="sxs-lookup"><span data-stu-id="38b08-168">No</span></span> |
| <span data-ttu-id="38b08-169">客户&nbsp;Y 订货人：May&nbsp;</span><span class="sxs-lookup"><span data-stu-id="38b08-169">Customer&nbsp;Y Orderer:&nbsp;May</span></span> | <span data-ttu-id="38b08-170">是</span><span class="sxs-lookup"><span data-stu-id="38b08-170">Yes</span></span> | <span data-ttu-id="38b08-171">无</span><span class="sxs-lookup"><span data-stu-id="38b08-171">No</span></span> | <span data-ttu-id="38b08-172">无</span><span class="sxs-lookup"><span data-stu-id="38b08-172">No</span></span> | <span data-ttu-id="38b08-173">无</span><span class="sxs-lookup"><span data-stu-id="38b08-173">No</span></span> | <span data-ttu-id="38b08-174">无</span><span class="sxs-lookup"><span data-stu-id="38b08-174">No</span></span> |

> [!NOTE]
> <span data-ttu-id="38b08-175">即使 Sam 和 Jane 都是为客户 X 工作的联系人，他们也只能查看他们自己下的订单，而看不到其他信息。</span><span class="sxs-lookup"><span data-stu-id="38b08-175">Even though both Sam and Jane are contacts who work for customer X, they can see only the orders that they themselves have placed and nothing else.</span></span> <span data-ttu-id="38b08-176">尽管 May 在系统中有一个订单，但由于她是未授权用户，因此她无法在客户门户中查看该订单。</span><span class="sxs-lookup"><span data-stu-id="38b08-176">Although May has an order in the system, she can't see that order in the Customer portal, because she is an unauthorized user.</span></span> <span data-ttu-id="38b08-177">（而且，她一定是通过客户门户以外的某个渠道下的订单。）</span><span class="sxs-lookup"><span data-stu-id="38b08-177">(Additionally, she must have placed the order through some channel other than the Customer portal.)</span></span>
