---
title: "管理供应商协作用户"
description: "本主题介绍您如何请求调配新供应商协作用户，以及如何添加新供应商协作联系人。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 380f1bcdf7109dc12fd898199033eac7710d863c
ms.lasthandoff: 03/31/2017


---

# <a name="manage-vendor-collaboration-users"></a>管理供应商协作用户

本主题介绍您如何请求调配新供应商协作用户，以及如何添加新供应商协作联系人。 

Microsoft Dynamics 365 for Operations 中的供应商协作界面向外部供应商公开有关采购订单、发票和托运存货的信息。 如果您是作为具有“**供应商管理员（外部）**”安全角色或类似权限的外部供应商，您可以创建新的供应商协作联系人和请求调配新用户。 如果您是作为采购专业人员，您也可以执行这些任务。 在本主题中，此角色是指在拥有 Dynamics 365 for Operations 实例的公司内部工作的采购专业人员。 有关如何使用供应商协作的详细信息，如果您为外部供应商，请参阅在客户的 [] (供应商协作工作 Dynamics 客户 365 operations.md) 供应商。  

有关如何使用供应商协作的详细信息，如果您是该采购专业，请参阅与外部供应商协作 [] (供应商协作工作) 的 vendors.md 外部供应商协作。

## <a name="add-new-vendor-collaboration-contacts"></a>添加新供应商协作联系人
如果希望某人拥有供应商协作的访问权限，必须先添加为供应商协作联系人。 您可能还想为公司中不会使用供应商协作的员工添加联系人。 例如，他们可能是其他类型的采购信息的联系人。 新的联系人。** **页面所有联系人添加，从**供应商协作** ** &gt; 联系人**菜单访问。 若要添加新的联系人：

1.  单击“**新建**”。
2.  输入联系人详细信息。
3.  选择他们在您的公司中所代表的法人，以及他们在将要协作的公司中将要合作的法人。 通过执行此**选择"我的法人在公司中/** **法人在客户**对公司中。
4.  单击“**创建**”。

如果要删除联系人，只可能删除您已经创建的联系人。

## <a name="vendor-collaboration-user-requests"></a>供应商协作用户请求
供应商协作用户请求可以由采购专业人员或外部供应商管理员提起。

-   如果您为外部供应商提交，您从**所有联系人**页的请求。**供应商协作**模块内。
-   如果您是采购专业人员，则从“**查看联系人**”页面提交请求。 为此，"供应商记录，在操作窗格的** **设置部分，选择的联系人** &gt; ** ** **查看联系。

您可以请求调配用户、停用用户或修改安全角色。 如果您是外部供应商管理员，您必须注册为您要为其提交用户请求的供应商帐户的联系人，且必须具有访问这些供应商帐户的供应商协作界面的权限。  

提交请求时，请求添加到“**供应商协作**”模块中的“**供应商协作用户请求**”列表和“**采购**”模块（外部用户不可访问采购模块）中的“**供应商协作用户请求**”列表。

### <a name="provision-a-user"></a>调配用户

您可以请求调配新用户之前，必须将新用户设置为一个或多个供应商帐户的联系人。 若要创建新供应商协作用户请求：

1.  **在所有联系人**页，单击**提供用户**供应商。
2.  输入该用户的电子邮件地址。 用户将使用该地址登录 Dynamics 365 for Operations。 如果电子邮件地址属于作为 Microsoft Azure 租户登记的域，则电子邮件地址必须为现有 Azure Active Directory (ADD) 帐户才能成功完成调配流程。 如果电子邮件地址不属于在 Microsoft Azure 登记的域，则必须在调配流程中创建 ADD，且新用户将收到邀请邮件。 与域的使用 ( @hotmail.com电子邮件地址、@gmail.com或 @comcast.net 无法用于登记工序用户的 Dynamics @hotmail.com。
3.  将“**允许供应商协作访问**”选项对用户需要访问的所有法人设置为“**是**”。
4.  在“**分配用户角色**”部分，选择新用户应有的安全角色的“**分配**”复选框。
5.  单击“**提交**”。

供应商银用户提交请求时，**供应商允许的协作访问**字段所选供应商帐户设置** **是，并且请求用户工作流开始。 作为工作流的一部分，在 Dynamics 365 for Operations 中创建新用户，并且分配安全角色。 此外还激活 Azure B2B 服务，启动 Azure 门户与“将新或现有 AAD 帐户与 Dynamics 365 for Operations 用户帐户相关联”之间的交互。

### <a name="inactivate-a-user"></a>停用用户

有两种方法可以删除用户对供应商协作的访问权限：

-   在供应商的“**联系人**”页面上，将“**允许供应商协作访问**”选项对联系人设置为“**否**”。 这可以对该人员作为联系人的每一个法人单独操作。 此选项仅可由采购专业人员使用。
-   通过提交“**停用供应商用户**”请求停用整个用户帐户。

请求用户停用：

1.  **在所有联系人**页，请单击**停用** **用户**供应商。
2.  在“**业务理由**”字段中写入备注。
3.  单击“**提交**”。

### <a name="modify-security-roles"></a>修改安全角色

**供应商维护用户角色**表页均相同。**供应商提供用户**页，除了列表安全角色可以编辑。  

请求的安全角色为用户修改：

1.  **在所有联系人**页，单击**维护** **供应商角色**用户。
2.  在“**业务理由**”字段中写入备注。
3.  在“**维护用户角色**”部分，选择要分配的安全角色，或者清除要删除的安全角色。
4.  Click **Submit**.



