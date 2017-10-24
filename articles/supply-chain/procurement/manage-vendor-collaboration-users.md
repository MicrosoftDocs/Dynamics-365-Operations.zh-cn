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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7dd5a1d9da4b648f07e87ad7921ac10ea92bb460
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="manage-vendor-collaboration-users"></a>管理供应商协作用户

[!include[banner](../includes/banner.md)]


本主题介绍您如何请求调配新供应商协作用户，以及如何添加新供应商协作联系人。 

Microsoft Dynamics 365 for Finance and Operations 中的供应商协作界面向外部供应商公开有关采购订单、发票和托运存货的信息。 如果您是作为具有“**供应商管理员（外部）**”安全角色或类似权限的外部供应商，您可以创建新的供应商协作联系人和请求调配新用户。 如果您是作为采购专业人员，您也可以执行这些任务。 在本主题中，此角色是指在拥有 Finance and Operations 实例的公司内部工作的采购专业人员。 有关如何使用供应商协作的详细信息，如果您是外部供应商，请参阅[具有客户的供应商](vendor-collaboration-work-customers-dynamics-365-operations.md)。  

。有关如何使用供应商协作的详细信息，如果您是采购专业人员，请参阅[供应商与外部供应商协作](vendor-collaboration-work-external-vendors.md)。

## <a name="add-new-vendor-collaboration-contacts"></a>添加新供应商协作联系人
如果希望某人拥有供应商协作的访问权限，必须先添加为供应商协作联系人。 您可能还想为公司中不会使用供应商协作的员工添加联系人。 例如，他们可能是其他类型的采购信息的联系人。 新联系人添加到**所有联系人**页面上，可从**供应商协作** &gt; > **联系人**菜单访问。 若要添加新的联系人：

1.  单击“**新建**”。
2.  输入联系人详细信息。
3.  选择他们在您的公司中所代表的法人，以及他们在将要协作的公司中将要合作的法人。 为此，您可以选择**我的公司中的法人**/**客户公司中的法人**对。
4.  单击“**创建**”。

如果要删除联系人，只可能删除您已经创建的联系人。

## <a name="vendor-collaboration-user-requests"></a>供应商协作用户请求
供应商协作用户请求可以由采购专业人员或外部供应商管理员提起。

-   如果您是外部供应商，则从**供应商协作**模块中的**所有联系人**页面提交请求。
-   如果您是采购专业人员，则从“**查看联系人**”页面提交请求。 为此，在供应商记录上，操作窗格的**设置**部分，选择**联系人** &gt; **查看联系人**。

您可以请求调配用户、停用用户或修改安全角色。 如果您是外部供应商管理员，您必须注册为您要为其提交用户请求的供应商帐户的联系人，且必须具有访问这些供应商帐户的供应商协作界面的权限。  

提交请求时，请求添加到“**供应商协作**”模块中的“**供应商协作用户请求**”列表和“**采购**”模块（外部用户不可访问采购模块）中的“**供应商协作用户请求**”列表。

### <a name="provision-a-user"></a>调配用户

您可以请求调配新用户之前，必须将新用户设置为一个或多个供应商帐户的联系人。 若要创建新供应商协作用户请求：

1.  在**所有联系人**页面，单击**调配供应商用户**。
2.  输入该用户的电子邮件地址。 用户将使用该地址登录 Finance and Operations。 如果电子邮件地址属于作为 Microsoft Azure 租户登记的域，则电子邮件地址必须为现有 Azure Active Directory (ADD) 帐户才能成功完成调配流程。 如果电子邮件地址不属于在 Microsoft Azure 登记的域，则必须在调配流程中创建 ADD，且新用户将收到邀请邮件。 域为 @hotmail.com、@gmail.com 或 @comcast.net 等的客户电子邮件不能用来注册 Finance and Operations 用户。
3.  将“**允许供应商协作访问**”选项对用户需要访问的所有法人设置为“**是**”。
4.  在“**分配用户角色**”部分，选择新用户应有的安全角色的“**分配**”复选框。
5.  单击“**提交**”。

提交供应商用户请求后，**允许供应商协作访问**字段对选定的供应商帐户设置为**是**，并开始用户请求工作流。 作为工作流的一部分，在 Finance and Operations 中创建新用户，并且分配安全角色。 此外还激活 Azure B2B 服务，启动 Azure 门户与“将新的或现有 AAD 帐户与 Finance and Operations 用户帐户相关联”之间的交互。

### <a name="inactivate-a-user"></a>停用用户

有两种方法可以删除用户对供应商协作的访问权限：

-   在供应商的“**联系人**”页面上，将“**允许供应商协作访问**”选项对联系人设置为“**否**”。 这可以对该人员作为联系人的每一个法人单独操作。 此选项仅可由采购专业人员使用。
-   通过提交“**停用供应商用户**”请求停用整个用户帐户。

若要请求停用用户：

1.  在**所有联系人**页面上，单击**停用****供应商用户**。
2.  在“**业务理由**”字段中写入备注。
3.  单击“**提交**”。

### <a name="modify-security-roles"></a>修改安全角色

**维护供应商用户角色**页面与**调配供应商用户**页面相同，除安全角色列表可编辑以外。  

若要请求修改用户的安全角色：

1.  在**所有联系人**页面上，单击**维护****供应商用户角色**。
2.  在“**业务理由**”字段中写入备注。
3.  在“**维护用户角色**”部分，选择要分配的安全角色，或者清除要删除的安全角色。
4.  单击“**提交**”。





