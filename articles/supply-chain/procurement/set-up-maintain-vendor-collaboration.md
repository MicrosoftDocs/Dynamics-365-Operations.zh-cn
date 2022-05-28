---
title: 设置和维护供应商协作
description: 本主题说明如何在 Dynamics 365 Supply Chain Management 中设置供应商协作。 另外还介绍了如何预配新的供应商协作用户和管理这些用户的安全角色。
author: GalynaFedorova
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirExternalRole, SysUserRequestListPage, VendVendorPortalUsers, WorkflowTableListPageRnr
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 220774
ms.assetid: 69d05e8b-7dc2-48ea-bc24-bea9ac963579
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4b59513d86426d3c1bfd759b9aabc331e58d5423
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677553"
---
# <a name="set-up-and-maintain-vendor-collaboration"></a>设置和维护供应商协作

[!include [banner](../includes/banner.md)]

供应商协作界面向外部供应商用户显示一组有限的有关采购订单、发票和托运存货的信息。 从此界面，供应商还可以回复询价 (RFQ)，以及查看和编辑基本公司信息。

本主题说明如何在 Dynamics 365 Supply Chain Management 中设置供应商协作。 另外还介绍了如何设置工作流来预配新的供应商协作用户，以及如何管理这些用户的安全角色。

> [!NOTE]
> 有关为供应商协作设置安全角色的信息仅适用于财务与运营的当前版本。 在 Microsoft Dynamics AX 7.0（2016 年 2 月）和 Microsoft Dynamics AX 应用程序版本 7.0.1（2016 年 5 月）中，使用 **供应商门户** 模块与供应商协作。 有关 Microsoft Dynamics AX 中供应商门户的用户权限的信息，请参阅[供应商门户用户安全性](configure-security-vendor-portal-users.md)。

## <a name="set-up-vendor-collaboration-security-roles"></a>设置供应商协作安全角色

采购专业人员或具有足够权限的供应商可以通过在联系人记录上启用 **预配供应商用户** 来请求将联系人预配为用户。 在预配过程中，将为新的外部用户选择用户权限，并提交新的供应商用户请求。 正确设置可供在供应商用户请求中选择的用户权限非常重要。 否则，供应商可能会被授予访问他们在 Supply Chain Management 中不应访问的信息的权限。

### <a name="set-up-the-security-roles-that-are-available-for-selection-when-a-new-user-request-is-used-for-a-contact-person"></a>设置新用户请求用于联系人时可供选择的安全角色

1. 选择 **系统管理** &gt; **安全** &gt; **外部角色**。
2. 选择 **新建**，然后选择安全角色和 **供应商** 当事方角色。

您可能需要添加 Supply Chain Management 中提供的 **供应商管理员（外部）** 和 **供应商（外部）** 角色。 或者，您可以使用您的公司已经创建的安全角色。

仅当供应商应能够创建新联系人、为新用户和用户信息更改提交供应商协作用户请求并通过工作流处理这些请求时，您才应该提供 **供应商管理员（外部）** 角色。

如果您计划手动设置供应商联系人和用户，就可以提供 **供应商（外部）角色**。 然后，此角色将成为唯一可以通过供应商用户请求请求的角色。

> [!NOTE]
> 当您手动创建新用户帐户时，将自动授予 **SystemUser** 角色。 因此，您必须删除该角色，然后分配 **SystemExternalUser** 角色。 如果通过供应商用户请求发起的工作流创建新用户帐户来预配新用户，将分配您为供应商协作设置的一个或多个角色和 **SystemExternalUser** 角色。

#### <a name="vendor-admin-external-security-role"></a>供应商管理员（外部）安全角色

**供应商管理员（外部）** 角色可用于维护供应商联系信息和请求预配新供应商协作用户的外部供应商。 具有此安全角色的外部用户可以执行以下任务：

- 查看和修改联系人信息，如此人的职务、电子邮件地址和电话号码。
- 将新联系人或现有联系人添加到其作为联系人的供应商帐户。
- 删除他们创建的任何联系人。
- 启用或禁用联系人与供应商帐户之间的关联。 联系人与供应商帐户之间的关联被禁用后，无法在新采购订单或其他文档中引用该联系人。
- 拒绝或允许联系人访问供应商协作界面上特定于供应商帐户的文档。 联系人与供应商帐户之间的关联被禁用后，将始终拒绝访问特定于供应商帐户的文档。
- 使用 **预配用户** 操作为联系人请求新的用户帐户。
- 请求停用联系人的用户帐户。
- 请求修改联系人的用户帐户以添加或删除安全角色。
- 查看 RFQ。

#### <a name="vendor-external-security-role"></a>供应商（外部）安全角色

**供应商（外部）角色** 可用于处理采购订单的外部供应商。 具有此安全角色的外部用户可以执行以下任务：

- 响应和查看有关采购订单的信息。
- 维护供应商协作发票。
- 查看托运库存。
- 查看和响应 RFQ。
- 查看供应商信息。

## <a name="set-up-security-roles-that-are-used-when-prospective-vendors-are-onboarded"></a>设置潜在供应商加入时使用的安全角色

要加入通过潜在供应商注册请求发起的供应商，您必须设置外部安全角色。 此角色将在由 **用户请求工作流（平台）** 类型的工作流控制的预配流程中分配给新用户。 有关详细信息，请参阅本主题后面的[设置工作流以处理供应商协作用户请求](#set-up-workflows-to-process-vendor-collaboration-user-requests)一节。

有关如何加入潜在供应商的信息，请参阅[加入供应商](vendor-onboarding.md)。

### <a name="set-up-a-security-role-that-is-used-when-a-new-prospective-vendor-user-request-is-submitted"></a>设置提交新的潜在供应商用户请求时使用的安全角色

1. 选择 **系统管理** > **安全** > **外部角色**。
2. 选择 **新建**，然后选择安全角色和 **潜在供应商** 当事方角色。

您应该添加 Supply Chain Management 中提供的 **供应商目标客户（外部）** 角色。

此安全角色将仅授予对新供应商注册向导的访问权限。

## <a name="set-up-workflows-to-process-vendor-collaboration-user-requests"></a>设置工作流以处理供应商协作用户请求

为帮助确保完成所有相关任务并给予适当的审批，您必须设置工作流来处理供应商协作用户请求。

供应商协作用户请求由具有 **供应商管理员（外部）** 安全角色或类似权限的外部供应商提交，或者由您公司的采购专业人员提交。 也可以在供应商加入流程中从潜在供应商注册请求生成。

请求有三种类型：

- 预配新用户的请求
- 禁用现有用户的请求
- 修改现有用户安全角色的请求

有关供应商协作用户请求的详细信息，请参阅[管理供应商协作用户](manage-vendor-collaboration-users.md)。

您必须创建两个或更多工作流来处理所有三种类型的供应商协作用户请求。 新工作流在 **用户工作流** 页面上创建。

### <a name="example-of-a-workflow-for-provisioning-new-users-and-modifying-security-roles"></a>预配新用户和修改安全角色的工作流示例

要处理创建新用户和修改安全角色的供应商用户请求，您可以在工作流的开头放一个分支条件。 这样，根据请求是创建新用户还是修改现有用户，将使用工作流的不同分支。

要设置此分支，请创建 **用户请求工作流（平台）** 类型的新工作流。 此工作流的分支可能包含以下元素。

#### <a name="branch-to-provision-new-users"></a>预配新用户的分支

1. 将审批任务分配给负责审批是否应授予新用户访问供应商协作信息的权限的人员。
2. 将任务分配给 Azure 门户中负责请求新的 Microsoft Azure Active Directory (Azure AD) 用户帐户的人员。 为此步骤使用预定义的 **发送 Azure B2B 用户邀请** 任务。 B2B 用户可自动导出到 Azure AD。 使用预定义的 **预配 Azure AD B2B 用户**。 有关详细信息，请参阅[将 B2B 用户导出到 Azure AD](../../fin-ops-core/dev-itpro/sysadmin/implement-b2b.md)。
3. 将审批任务分配给向 Azure 上载的人员。 如果未成功创建帐户，此人将拒绝任务并结束工作流。 如果您已包含通过 B2B 应用程序编程接口 (API) 自动将新用户帐户导出到 Azure 的步骤，则可以跳过此审批任务。
4. 添加预配新用户的自动化任务。 为此步骤使用预定义的 **自动预配用户** 任务。
5. 添加通知新用户的任务。 您可能希望向新用户发送一封欢迎电子邮件，其中包含 Supply Chain Management 的 URL。 此电子邮件可以使用您在 **电子邮件消息** 页面上创建的模板，然后在 **用户工作流参数** 页面上进行选择。 此模板可以包括 **%portalURL%** 标记。 生成欢迎电子邮件时，此标记将替换为 Supply Chain Management 租户的 URL。

    > [!NOTE]
    > 此工作流可用于涉及用户加入的多个场景。 例如，当潜在供应商或联系人需要供应商协作帐户时，可以使用它。 因此，您应该将电子邮件表述为可用于多个目的的一般语句。

#### <a name="branch-to-modify-security-roles"></a>修改安全角色的分支

1. 将审批任务分配给负责审批安全角色更改的人员。
2. 添加添加或删除相关安全角色的自动化任务。 为此步骤使用 **自动预配用户** 任务。

### <a name="example-of-a-workflow-for-inactivating-a-user"></a>停用用户的工作流示例

创建 **停用用户请求工作流平台** 类型的工作流，然后添加以下任务。

1. 将审批任务分配给负责接受停用用户请求的人员。 您可以添加条件来自动执行此审批步骤。
2. 添加停用用户的自动化任务。 为此步骤使用 **自动停用用户** 任务。
3. 添加需要的任何清理任务。 例如，您可以在 Azure 门户中添加从目录中删除帐户的任务。

## <a name="enable-vendor-collaboration-for-a-specific-vendor"></a>为特定供应商启用供应商协作

在为将要使用供应商协作的人员创建用户帐户之前，您必须设置供应商，使其可以使用供应商协作。 在 **供应商** 页面的 **常规** 选项卡上，设置 **协作激活** 字段。 选项如下：

- **活动（自动确认采购订单）**– 在供应商不请求更改的情况下接受采购订单时，自动确认采购订单。
- **活动（不自动确认采购订单）**– 供应商接受采购订单后，必须由您的组织手动确认采购订单。

> [!NOTE]
> 您的公司中的采购专业人员也可以完成此任务。

## <a name="troubleshoot-the-provisioning-of-new-vendor-collaboration-users"></a>预配新供应商协作用户故障排除

新供应商协作用户通过您设置的工作流被预配为处理 **预配供应商用户** 类型的供应商协作用户请求。

如果新供应商协作用户的电子邮件地址属于在 Azure 中注册为租户的域（即它是托管域帐户），该电子邮件地址必须是现有的 Azure AD 帐户。 否则，无法完成预配流程。

有关 Azure AD 帐户管理工作流中 **发送 Azure B2B 用户邀请** 任务中使用的流程的详细信息，请参阅 [Azure Active Directory B2B 协作](/azure/active-directory/external-identities/what-is-b2b)。

## <a name="additional-resources"></a>其他资源

[供应商与外部供应商的协作](vendor-collaboration-work-external-vendors.md)

观看有关供应商加入流程的短视频：[加入新供应商](https://www.youtube.com/watch?v=0KUc3AGaTKk&feature=youtu.be)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
