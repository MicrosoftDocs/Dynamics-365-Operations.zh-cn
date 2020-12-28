---
title: 管理供应商协作用户
description: 本主题介绍您如何请求调配新供应商协作用户，以及如何添加新供应商协作联系人。
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 29930fdb65f96e281e0f0f01db41ec1475ad81c2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423282"
---
# <a name="manage-vendor-collaboration-users"></a><span data-ttu-id="34f66-103">管理供应商协作用户</span><span class="sxs-lookup"><span data-stu-id="34f66-103">Manage vendor collaboration users</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34f66-104">本主题介绍您如何请求调配新供应商协作用户，以及如何添加新供应商协作联系人。</span><span class="sxs-lookup"><span data-stu-id="34f66-104">This topic describes how you can request the provisioning of new vendor collaboration users, and how to add new vendor collaboration contacts.</span></span> 

<span data-ttu-id="34f66-105">Dynamics 365 Supply Chain Management 中的供应商协作界面向外部供应商公开有关采购订单、发票和托运存货的信息。</span><span class="sxs-lookup"><span data-stu-id="34f66-105">The vendor collaboration interface in Dynamics 365 Supply Chain Management exposes information about purchase orders, invoices, and consignment stock to external vendors.</span></span> <span data-ttu-id="34f66-106">如果您是作为具有 **供应商管理员（外部）** 安全角色或类似权限的外部供应商，您可以创建新的供应商协作联系人和请求调配新用户。</span><span class="sxs-lookup"><span data-stu-id="34f66-106">You can create new vendor collaboration contacts and request that new users are provisioned if you're working as an external vendor with the **Vendor admin (external)** security role, or similar permissions.</span></span> <span data-ttu-id="34f66-107">如果您是作为采购专业人员，您也可以执行这些任务。</span><span class="sxs-lookup"><span data-stu-id="34f66-107">You can also perform these tasks if you're working as a procurement professional.</span></span> <span data-ttu-id="34f66-108">在本主题中，此角色是指在拥有 Supply Chain Management 实例的公司内部工作的采购专业人员。</span><span class="sxs-lookup"><span data-stu-id="34f66-108">In this topic, this role refers to a procurement professional who is working within the company that owns the instance of Supply Chain Management.</span></span> <span data-ttu-id="34f66-109">有关如何使用供应商协作的详细信息，如果您是外部供应商，请参阅[供应商与客户的协作](vendor-collaboration-work-customers-dynamics-365-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="34f66-109">For more information about how to use vendor collaboration if you're an external vendor, see [Vendor collaboration with customers](vendor-collaboration-work-customers-dynamics-365-operations.md).</span></span>  

<span data-ttu-id="34f66-110">。有关如何使用供应商协作的详细信息，如果您是采购专业人员，请参阅[供应商与外部供应商协作](vendor-collaboration-work-external-vendors.md)。</span><span class="sxs-lookup"><span data-stu-id="34f66-110">For more information about how to use vendor collaboration if you're a procurement professional, see [Vendor collaboration with external vendors](vendor-collaboration-work-external-vendors.md).</span></span>

## <a name="add-new-vendor-collaboration-contacts"></a><span data-ttu-id="34f66-111">添加新供应商协作联系人</span><span class="sxs-lookup"><span data-stu-id="34f66-111">Add new vendor collaboration contacts</span></span>
<span data-ttu-id="34f66-112">如果希望某人拥有供应商协作的访问权限，必须先添加为供应商协作联系人。</span><span class="sxs-lookup"><span data-stu-id="34f66-112">If you want someone to have access to vendor collaboration they first have to be added as a vendor collaboration contact.</span></span> <span data-ttu-id="34f66-113">您可能还想为公司中不会使用供应商协作的员工添加联系人。</span><span class="sxs-lookup"><span data-stu-id="34f66-113">You may also want to add contacts for employees in your company who won't use vendor collaboration.</span></span> <span data-ttu-id="34f66-114">例如，他们可能是其他类型的采购信息的联系人。</span><span class="sxs-lookup"><span data-stu-id="34f66-114">For example, they could be the point of contact for other kinds of procurement information.</span></span> <span data-ttu-id="34f66-115">新联系人添加到 **所有联系人** 页面上，可从 **供应商协作** &gt; > **联系人** 菜单访问。</span><span class="sxs-lookup"><span data-stu-id="34f66-115">New contacts are added on the **All contacts** page, which is accessed from the **Vendor collaboration** &gt; **Contacts** menu.</span></span> <span data-ttu-id="34f66-116">若要添加新的联系人：</span><span class="sxs-lookup"><span data-stu-id="34f66-116">To add a new contact:</span></span>

1.  <span data-ttu-id="34f66-117">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="34f66-117">Click **New.**</span></span>
2.  <span data-ttu-id="34f66-118">输入联系人详细信息。</span><span class="sxs-lookup"><span data-stu-id="34f66-118">Enter the contact person details.</span></span>
3.  <span data-ttu-id="34f66-119">选择他们在您的公司中所代表的法人，以及他们在将要协作的公司中将要合作的法人。</span><span class="sxs-lookup"><span data-stu-id="34f66-119">Choose which legal entity they're representing in your company, and which legal entity they'll work with in the company that they'll collaborate with.</span></span> <span data-ttu-id="34f66-120">为此，您可以选择 **我的公司中的法人**/**客户公司中的法人** 对。</span><span class="sxs-lookup"><span data-stu-id="34f66-120">You do this by selecting a **Legal entity in my company**/**Legal entity in customer company** pair.</span></span>
4.  <span data-ttu-id="34f66-121">单击 **创建**。</span><span class="sxs-lookup"><span data-stu-id="34f66-121">Click **Create.**</span></span>

<span data-ttu-id="34f66-122">如果要删除联系人，只可能删除您已经创建的联系人。</span><span class="sxs-lookup"><span data-stu-id="34f66-122">If you want to delete a contact, it's only possible to delete the ones that you've created.</span></span>

## <a name="vendor-collaboration-user-requests"></a><span data-ttu-id="34f66-123">供应商协作用户请求</span><span class="sxs-lookup"><span data-stu-id="34f66-123">Vendor collaboration user requests</span></span>
<span data-ttu-id="34f66-124">供应商协作用户请求可以由采购专业人员或外部供应商管理员提起。</span><span class="sxs-lookup"><span data-stu-id="34f66-124">Vendor collaboration user requests can be raised by a procurement professional, or by an external vendor administrator.</span></span>

-   <span data-ttu-id="34f66-125">如果您是外部供应商，则从 **供应商协作** 模块中的 **所有联系人** 页面提交请求。</span><span class="sxs-lookup"><span data-stu-id="34f66-125">If you're an external vendor, you submit requests from the **All contacts** page within the **Vendor collaboration** module.</span></span>
-   <span data-ttu-id="34f66-126">如果您是采购专业人员，则从 **查看联系人** 页面提交请求。</span><span class="sxs-lookup"><span data-stu-id="34f66-126">If you're a procurement professional, you submit requests from the **View contacts** page.</span></span> <span data-ttu-id="34f66-127">为此，在供应商记录上，操作窗格的 **设置** 部分，选择 **联系人** &gt; **查看联系人**。</span><span class="sxs-lookup"><span data-stu-id="34f66-127">To do this, on the vendor record, in the **Setup** section on the Action Pane, select **Contacts** &gt; **View contacts**.</span></span>

<span data-ttu-id="34f66-128">您可以请求调配用户、停用用户或修改安全角色。</span><span class="sxs-lookup"><span data-stu-id="34f66-128">You can make a request to provision a user, to inactivate a user, or to modify security roles.</span></span> <span data-ttu-id="34f66-129">如果您是外部供应商管理员，您必须注册为您要为其提交用户请求的供应商帐户的联系人，且必须具有访问这些供应商帐户的供应商协作界面的权限。</span><span class="sxs-lookup"><span data-stu-id="34f66-129">If you're an external vendor administrator, you must be registered as a contact person for the vendor accounts that you want to make user requests for, and you must have access to the vendor collaboration interface for those vendor accounts.</span></span>  

<span data-ttu-id="34f66-130">提交请求时，请求添加到 **供应商协作** 模块中的 **供应商协作用户请求** 列表和 **采购** 模块（外部用户不可访问采购模块）中的 **供应商协作用户请求** 列表。</span><span class="sxs-lookup"><span data-stu-id="34f66-130">When a request is submitted it is added to the **Vendor collaboration user requests** list in the **Vendor collaboration** module, and to the **Vendor collaboration user request** list in the **Procurement and sourcing** module (the Procurement and sourcing module is not accessible to external users).</span></span>

### <a name="provision-a-user"></a><span data-ttu-id="34f66-131">调配用户</span><span class="sxs-lookup"><span data-stu-id="34f66-131">Provision a user</span></span>

<span data-ttu-id="34f66-132">您可以请求调配新用户之前，必须将新用户设置为一个或多个供应商帐户的联系人。</span><span class="sxs-lookup"><span data-stu-id="34f66-132">Before you can request that a new user is provisioned, that person must be set up as a contact for one or more vendor accounts.</span></span> <span data-ttu-id="34f66-133">若要创建新供应商协作用户请求：</span><span class="sxs-lookup"><span data-stu-id="34f66-133">To create a request for a new vendor collaboration user:</span></span>

1. <span data-ttu-id="34f66-134">在 **所有联系人** 页面，单击 **调配供应商用户**。</span><span class="sxs-lookup"><span data-stu-id="34f66-134">On the **All contacts** page, click **Provision vendor user**.</span></span>
2. <span data-ttu-id="34f66-135">输入该用户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="34f66-135">Enter an email address for the user.</span></span> <span data-ttu-id="34f66-136">用户将使用此地址登录 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="34f66-136">This address will be used by the user to sign in to Supply Chain Management.</span></span> <span data-ttu-id="34f66-137">如果电子邮件地址属于作为 Microsoft Azure 租户登记的域，则电子邮件地址必须为现有 Azure Active Directory (AAD) 帐户才能成功完成调配流程。</span><span class="sxs-lookup"><span data-stu-id="34f66-137">If the email address belongs to a domain registered as a tenant with Microsoft Azure, then the email address has to be an existing Azure Active Directory (AAD) account in order for the provisioning process to complete successfully.</span></span> <span data-ttu-id="34f66-138">如果电子邮件地址不属于在 Microsoft Azure 登记的域，则必须在调配流程中创建 AAD，且新用户将收到邀请邮件。</span><span class="sxs-lookup"><span data-stu-id="34f66-138">If the email address does not belong to a domain registered with Microsoft Azure, an AAD account will be created as part of the provisioning process and the new user will receive an invitation mail.</span></span> <span data-ttu-id="34f66-139">域为 @hotmail.com、@gmail.com 或 @comcast.net 等的客户电子邮件不能用来注册用户。</span><span class="sxs-lookup"><span data-stu-id="34f66-139">Consumer email addresses with domains such as @hotmail.com, @gmail.com, or @comcast.net cannot be used to register a  user.</span></span>
3. <span data-ttu-id="34f66-140">将 **允许供应商协作访问** 选项对用户需要访问的所有法人设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="34f66-140">Set the **Vendor collaboration access allowed** option to **Yes** for all the legal entities that the user needs access to.</span></span>
4. <span data-ttu-id="34f66-141">在 **分配用户角色** 部分，选择新用户应有的安全角色的 **分配** 复选框。</span><span class="sxs-lookup"><span data-stu-id="34f66-141">In the **Assign user roles** section, select the **Assign** check box for the security roles that the new user should have.</span></span>
5. <span data-ttu-id="34f66-142">单击 **提交**。</span><span class="sxs-lookup"><span data-stu-id="34f66-142">Click **Submit**.</span></span>

<span data-ttu-id="34f66-143">提交供应商用户请求后，**允许供应商协作访问** 字段对选定的供应商帐户设置为 **是**，并开始用户请求工作流。</span><span class="sxs-lookup"><span data-stu-id="34f66-143">When the vendor user request is submitted, the **Vendor collaboration access allowed** field is set to **Yes** for the selected vendor account and a user request workflow is started.</span></span> <span data-ttu-id="34f66-144">作为工作流的一部分，创建新用户，并且分配安全角色。</span><span class="sxs-lookup"><span data-stu-id="34f66-144">As part of the workflow, a new user is created, and security roles are assigned.</span></span> <span data-ttu-id="34f66-145">此外还激活 Azure B2B 服务，启动 Azure 门户与“将新的或现有 AAD 帐户与 Supply Chain Management 用户帐户相关联”之间的交互。</span><span class="sxs-lookup"><span data-stu-id="34f66-145">In addition, an Azure B2B service is activated which initiates interaction with Azure portal and associates a new or existing AAD account with the Supply Chain Management user account.</span></span> <span data-ttu-id="34f66-146">有关详细信息，请参阅 [Azure AD B2B 协作简介](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b)。</span><span class="sxs-lookup"><span data-stu-id="34f66-146">For more information, see [What is Azure AD B2B collaboration?](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b).</span></span>

### <a name="inactivate-a-user"></a><span data-ttu-id="34f66-147">停用用户</span><span class="sxs-lookup"><span data-stu-id="34f66-147">Inactivate a user</span></span>

<span data-ttu-id="34f66-148">有两种方法可以删除用户对供应商协作的访问权限：</span><span class="sxs-lookup"><span data-stu-id="34f66-148">There are two ways to remove access to vendor collaboration for a user:</span></span>

-   <span data-ttu-id="34f66-149">在供应商的 **联系人** 页面上，将 **允许供应商协作访问** 选项对联系人设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="34f66-149">On the **Contacts** page for the vendor, set the **Vendor collaboration access allowed** option to **No** for the contact.</span></span> <span data-ttu-id="34f66-150">这可以对该人员作为联系人的每一个法人单独操作。</span><span class="sxs-lookup"><span data-stu-id="34f66-150">This can be done individually per legal entity that the person is a contact for.</span></span> <span data-ttu-id="34f66-151">此选项仅可由采购专业人员使用。</span><span class="sxs-lookup"><span data-stu-id="34f66-151">This option can only be used by procurement professionals.</span></span>
-   <span data-ttu-id="34f66-152">通过提交 **停用供应商用户** 请求停用整个用户帐户。</span><span class="sxs-lookup"><span data-stu-id="34f66-152">Inactivate the entire user account, by submitting an **Inactivate vendor user** request.</span></span>

<span data-ttu-id="34f66-153">若要请求停用用户：</span><span class="sxs-lookup"><span data-stu-id="34f66-153">To request that a user is inactivated:</span></span>

1.  <span data-ttu-id="34f66-154">在 **所有联系人** 页面上，单击 **停用** 供 **应商用户**。</span><span class="sxs-lookup"><span data-stu-id="34f66-154">On the **All contacts** page, click **Inactivate** **vendor user**.</span></span>
2.  <span data-ttu-id="34f66-155">在 **业务理由** 字段中写入备注。</span><span class="sxs-lookup"><span data-stu-id="34f66-155">Write a comment in the **Business justification** field.</span></span>
3.  <span data-ttu-id="34f66-156">单击 **提交**。</span><span class="sxs-lookup"><span data-stu-id="34f66-156">Click **Submit**.</span></span>

### <a name="modify-security-roles"></a><span data-ttu-id="34f66-157">修改安全角色</span><span class="sxs-lookup"><span data-stu-id="34f66-157">Modify security roles</span></span>

<span data-ttu-id="34f66-158">**维护供应商用户角色** 页面与 **调配供应商用户** 页面相同，除安全角色列表可编辑以外。</span><span class="sxs-lookup"><span data-stu-id="34f66-158">The **Maintain vendor user roles** page is the same as the **Provision vendor user** page except that the list of security roles can be edited.</span></span>  

<span data-ttu-id="34f66-159">若要请求修改用户的安全角色：</span><span class="sxs-lookup"><span data-stu-id="34f66-159">To request that the security roles are modified for a user:</span></span>

1.  <span data-ttu-id="34f66-160">在 **所有联系人** 页面上，单击 **维护** 供 **应商用户角色**。</span><span class="sxs-lookup"><span data-stu-id="34f66-160">On the **All contacts** page, click **Maintain** **vendor user roles**.</span></span>
2.  <span data-ttu-id="34f66-161">在 **业务理由** 字段中写入备注。</span><span class="sxs-lookup"><span data-stu-id="34f66-161">Write a comment in the **Business justification** field.</span></span>
3.  <span data-ttu-id="34f66-162">在 **维护用户角色** 部分，选择要分配的安全角色，或者清除要删除的安全角色。</span><span class="sxs-lookup"><span data-stu-id="34f66-162">In the **Maintain user roles** section, select the security roles that you want to assign, or clear the ones that you want to remove.</span></span>
4.  <span data-ttu-id="34f66-163">单击 **提交**。</span><span class="sxs-lookup"><span data-stu-id="34f66-163">Click **Submit**.</span></span>




