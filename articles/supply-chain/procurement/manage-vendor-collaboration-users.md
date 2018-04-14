---
title: "管理供应商协作用户"
description: "本主题介绍您如何请求调配新供应商协作用户，以及如何添加新供应商协作联系人。"
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 932e158f35f535775647795b19128f63db378eea
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="manage-vendor-collaboration-users"></a><span data-ttu-id="3e7f6-103">管理供应商协作用户</span><span class="sxs-lookup"><span data-stu-id="3e7f6-103">Manage vendor collaboration users</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="3e7f6-104">本主题介绍您如何请求调配新供应商协作用户，以及如何添加新供应商协作联系人。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-104">This topic describes how you can request the provisioning of new vendor collaboration users, and how to add new vendor collaboration contacts.</span></span> 

<span data-ttu-id="3e7f6-105">Microsoft Dynamics 365 for Finance and Operations 中的供应商协作界面向外部供应商公开有关采购订单、发票和托运存货的信息。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-105">The vendor collaboration interface in Microsoft Dynamics 365 for Finance and Operations exposes information about purchase orders, invoices, and consignment stock to external vendors.</span></span> <span data-ttu-id="3e7f6-106">如果您是作为具有“**供应商管理员（外部）**”安全角色或类似权限的外部供应商，您可以创建新的供应商协作联系人和请求调配新用户。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-106">You can create new vendor collaboration contacts and request that new users are provisioned if you're working as an external vendor with the **Vendor admin (external)** security role, or similar permissions.</span></span> <span data-ttu-id="3e7f6-107">如果您是作为采购专业人员，您也可以执行这些任务。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-107">You can also perform these tasks if you're working as a procurement professional.</span></span> <span data-ttu-id="3e7f6-108">在本主题中，此角色是指在拥有 Finance and Operations 实例的公司内部工作的采购专业人员。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-108">In this topic, this role refers to a procurement professional who is working within the company that owns the instance of Finance and Operations.</span></span> <span data-ttu-id="3e7f6-109">有关如何使用供应商协作的详细信息，如果您是外部供应商，请参阅[具有客户的供应商](vendor-collaboration-work-customers-dynamics-365-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-109">For more information about how to use vendor collaboration if you're an external vendor, see [Vendor with customers](vendor-collaboration-work-customers-dynamics-365-operations.md).</span></span>  

<span data-ttu-id="3e7f6-110">。有关如何使用供应商协作的详细信息，如果您是采购专业人员，请参阅[供应商与外部供应商协作](vendor-collaboration-work-external-vendors.md)。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-110">For more information about how to use vendor collaboration if you're a procurement professional, see [Vendor collaboration to with external vendors](vendor-collaboration-work-external-vendors.md).</span></span>

## <a name="add-new-vendor-collaboration-contacts"></a><span data-ttu-id="3e7f6-111">添加新供应商协作联系人</span><span class="sxs-lookup"><span data-stu-id="3e7f6-111">Add new vendor collaboration contacts</span></span>
<span data-ttu-id="3e7f6-112">如果希望某人拥有供应商协作的访问权限，必须先添加为供应商协作联系人。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-112">If you want someone to have access to vendor collaboration they first have to be added as a vendor collaboration contact.</span></span> <span data-ttu-id="3e7f6-113">您可能还想为公司中不会使用供应商协作的员工添加联系人。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-113">You may also want to add contacts for employees in your company who won't use vendor collaboration.</span></span> <span data-ttu-id="3e7f6-114">例如，他们可能是其他类型的采购信息的联系人。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-114">For example, they could be the point of contact for other kinds of procurement information.</span></span> <span data-ttu-id="3e7f6-115">新联系人添加到**所有联系人**页面上，可从**供应商协作** &gt; > **联系人**菜单访问。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-115">New contacts are added on the **All contacts** page, which is accessed from the **Vendor collaboration** &gt; **Contacts** menu.</span></span> <span data-ttu-id="3e7f6-116">若要添加新的联系人：</span><span class="sxs-lookup"><span data-stu-id="3e7f6-116">To add a new contact:</span></span>

1.  <span data-ttu-id="3e7f6-117">单击“**新建**”。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-117">Click **New.**</span></span>
2.  <span data-ttu-id="3e7f6-118">输入联系人详细信息。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-118">Enter the contact person details.</span></span>
3.  <span data-ttu-id="3e7f6-119">选择他们在您的公司中所代表的法人，以及他们在将要协作的公司中将要合作的法人。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-119">Choose which legal entity they're representing in your company, and which legal entity they'll work with in the company that they'll collaborate with.</span></span> <span data-ttu-id="3e7f6-120">为此，您可以选择**我的公司中的法人**/**客户公司中的法人**对。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-120">You do this by selecting a **Legal entity in my company**/**Legal entity in customer company** pair.</span></span>
4.  <span data-ttu-id="3e7f6-121">单击“**创建**”。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-121">Click **Create.**</span></span>

<span data-ttu-id="3e7f6-122">如果要删除联系人，只可能删除您已经创建的联系人。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-122">If you want to delete a contact, it's only possible to delete the ones that you've created.</span></span>

## <a name="vendor-collaboration-user-requests"></a><span data-ttu-id="3e7f6-123">供应商协作用户请求</span><span class="sxs-lookup"><span data-stu-id="3e7f6-123">Vendor collaboration user requests</span></span>
<span data-ttu-id="3e7f6-124">供应商协作用户请求可以由采购专业人员或外部供应商管理员提起。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-124">Vendor collaboration user requests can be raised by a procurement professional, or by an external vendor administrator.</span></span>

-   <span data-ttu-id="3e7f6-125">如果您是外部供应商，则从**供应商协作**模块中的**所有联系人**页面提交请求。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-125">If you're an external vendor, you submit requests from the **All contacts** page within the **Vendor collaboration** module.</span></span>
-   <span data-ttu-id="3e7f6-126">如果您是采购专业人员，则从“**查看联系人**”页面提交请求。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-126">If you're a procurement professional, you submit requests from the **View contacts** page.</span></span> <span data-ttu-id="3e7f6-127">为此，在供应商记录上，操作窗格的**设置**部分，选择**联系人** &gt; **查看联系人**。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-127">To do this, on the vendor record, in the **Setup** section in the Action pane, select **Contacts** &gt; **View contacts**.</span></span>

<span data-ttu-id="3e7f6-128">您可以请求调配用户、停用用户或修改安全角色。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-128">You can make a request to provision a user, to inactivate a user, or to modify security roles.</span></span> <span data-ttu-id="3e7f6-129">如果您是外部供应商管理员，您必须注册为您要为其提交用户请求的供应商帐户的联系人，且必须具有访问这些供应商帐户的供应商协作界面的权限。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-129">If you're an external vendor administrator, you must be registered as a contact person for the vendor accounts that you want to make user requests for, and you must have access to the vendor collaboration interface for those vendor accounts.</span></span>  

<span data-ttu-id="3e7f6-130">提交请求时，请求添加到“**供应商协作**”模块中的“**供应商协作用户请求**”列表和“**采购**”模块（外部用户不可访问采购模块）中的“**供应商协作用户请求**”列表。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-130">When a request is submitted it is added to the **Vendor collaboration user requests** list in the **Vendor collaboration** module, and to the **Vendor collaboration user request** list in the **Procurement and sourcing** module (the Procurement and sourcing module is not accessible to external users).</span></span>

### <a name="provision-a-user"></a><span data-ttu-id="3e7f6-131">调配用户</span><span class="sxs-lookup"><span data-stu-id="3e7f6-131">Provision a user</span></span>

<span data-ttu-id="3e7f6-132">您可以请求调配新用户之前，必须将新用户设置为一个或多个供应商帐户的联系人。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-132">Before you can request that a new user is provisioned, that person must be set up as a contact for one or more vendor accounts.</span></span> <span data-ttu-id="3e7f6-133">若要创建新供应商协作用户请求：</span><span class="sxs-lookup"><span data-stu-id="3e7f6-133">To create a request for a new vendor collaboration user:</span></span>

1. <span data-ttu-id="3e7f6-134">在**所有联系人**页面，单击**调配供应商用户**。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-134">On the **All contacts** page, click **Provision vendor user**.</span></span>
2. <span data-ttu-id="3e7f6-135">输入该用户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-135">Enter an email address for the user.</span></span> <span data-ttu-id="3e7f6-136">用户将使用该地址登录 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-136">This address will be used by the user to log onto Finance and Operations.</span></span> <span data-ttu-id="3e7f6-137">如果电子邮件地址属于作为 Microsoft Azure 租户登记的域，则电子邮件地址必须为现有 Azure Active Directory (AAD) 帐户才能成功完成调配流程。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-137">If the email address belongs to a domain registered as a tenant with Microsoft Azure, then the email address has to be an existing Azure Active Directory (AAD) account in order for the provisioning process to complete successfully.</span></span> <span data-ttu-id="3e7f6-138">如果电子邮件地址不属于在 Microsoft Azure 登记的域，则必须在调配流程中创建 ADD，且新用户将收到邀请邮件。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-138">If the email address does not belong to a domain registered with Microsoft Azure, an ADD account will be created as part of the provisioning process and the new user will receive an invitation mail.</span></span> <span data-ttu-id="3e7f6-139">域为 @hotmail.com、@gmail.com 或 @comcast.net 等的客户电子邮件不能用来注册 Finance and Operations 用户。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-139">Consumer email addresses with domains such as @hotmail.com, @gmail.com, or @comcast.net cannot be used to register a Finance and Operations user.</span></span>
3. <span data-ttu-id="3e7f6-140">将“**允许供应商协作访问**”选项对用户需要访问的所有法人设置为“**是**”。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-140">Set the **Vendor collaboration access allowed** option to **Yes** for all the legal entities that the user needs access to.</span></span>
4. <span data-ttu-id="3e7f6-141">在“**分配用户角色**”部分，选择新用户应有的安全角色的“**分配**”复选框。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-141">In the **Assign user roles** section, select the **Assign** check box for the security roles that the new user should have.</span></span>
5. <span data-ttu-id="3e7f6-142">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-142">Click **Submit**.</span></span>

<span data-ttu-id="3e7f6-143">提交供应商用户请求后，**允许供应商协作访问**字段对选定的供应商帐户设置为**是**，并开始用户请求工作流。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-143">When the vendor user request is submitted, the **Vendor collaboration access allowed** field is set to **Yes** for the selected vendor account and a user request workflow is started.</span></span> <span data-ttu-id="3e7f6-144">作为工作流的一部分，在 Finance and Operations 中创建新用户，并且分配安全角色。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-144">As part of the workflow, a new user is created in Finance and Operations, and security roles are assigned.</span></span> <span data-ttu-id="3e7f6-145">此外还激活 Azure B2B 服务，启动 Azure 门户与“将新的或现有 AAD 帐户与 Finance and Operations 用户帐户相关联”之间的交互。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-145">In addition, an Azure B2B service is activated which initiates interaction with Azure portal and associates a new or existing AAD account with the Finance and Operations user account.</span></span> <span data-ttu-id="3e7f6-146">有关详细信息，请参阅 [Azure AD B2B 协作简介](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b)。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-146">For more information, see [What is Azure AD B2B collaboration?](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b).</span></span>

### <a name="inactivate-a-user"></a><span data-ttu-id="3e7f6-147">停用用户</span><span class="sxs-lookup"><span data-stu-id="3e7f6-147">Inactivate a user</span></span>

<span data-ttu-id="3e7f6-148">有两种方法可以删除用户对供应商协作的访问权限：</span><span class="sxs-lookup"><span data-stu-id="3e7f6-148">There are two ways to remove access to vendor collaboration for a user:</span></span>

-   <span data-ttu-id="3e7f6-149">在供应商的“**联系人**”页面上，将“**允许供应商协作访问**”选项对联系人设置为“**否**”。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-149">On the **Contacts** page for the vendor, set the **Vendor collaboration access allowed** option to **No** for the contact.</span></span> <span data-ttu-id="3e7f6-150">这可以对该人员作为联系人的每一个法人单独操作。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-150">This can be done individually per legal entity that the person is a contact for.</span></span> <span data-ttu-id="3e7f6-151">此选项仅可由采购专业人员使用。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-151">This option can only be used by procurement professionals.</span></span>
-   <span data-ttu-id="3e7f6-152">通过提交“**停用供应商用户**”请求停用整个用户帐户。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-152">Inactivate the entire user account, by submitting an **Inactivate vendor user** request.</span></span>

<span data-ttu-id="3e7f6-153">若要请求停用用户：</span><span class="sxs-lookup"><span data-stu-id="3e7f6-153">To request that a user is inactivated:</span></span>

1.  <span data-ttu-id="3e7f6-154">在**所有联系人**页面上，单击**停用供应商用户**。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-154">On the **All contacts** page, click **Inactivate** **vendor user**.</span></span>
2.  <span data-ttu-id="3e7f6-155">在“**业务理由**”字段中写入备注。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-155">Write a comment in the **Business justification** field.</span></span>
3.  <span data-ttu-id="3e7f6-156">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-156">Click **Submit**.</span></span>

### <a name="modify-security-roles"></a><span data-ttu-id="3e7f6-157">修改安全角色</span><span class="sxs-lookup"><span data-stu-id="3e7f6-157">Modify security roles</span></span>

<span data-ttu-id="3e7f6-158">**维护供应商用户角色**页面与**调配供应商用户**页面相同，除安全角色列表可编辑以外。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-158">The **Maintain vendor user roles** page is the same as the **Provision vendor user** page except that the list of security roles can be edited.</span></span>  

<span data-ttu-id="3e7f6-159">若要请求修改用户的安全角色：</span><span class="sxs-lookup"><span data-stu-id="3e7f6-159">To request that the security roles are modified for a user:</span></span>

1.  <span data-ttu-id="3e7f6-160">在**所有联系人**页面上，单击**维护供应商用户角色**。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-160">On the **All contacts** page, click **Maintain** **vendor user roles**.</span></span>
2.  <span data-ttu-id="3e7f6-161">在“**业务理由**”字段中写入备注。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-161">Write a comment in the **Business justification** field.</span></span>
3.  <span data-ttu-id="3e7f6-162">在“**维护用户角色**”部分，选择要分配的安全角色，或者清除要删除的安全角色。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-162">In the **Maintain user roles** section, select the security roles that you want to assign, or clear the ones that you want to remove.</span></span>
4.  <span data-ttu-id="3e7f6-163">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="3e7f6-163">Click **Submit**.</span></span>





