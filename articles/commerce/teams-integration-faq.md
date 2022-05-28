---
title: Dynamics 365 Commerce 和 Microsoft Teams 集成常见问题解答
description: 本主题提供对有关 Microsoft Dynamics 365 Commerce 和 Microsoft Teams 集成的常见问题的解答。
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 16ad6cec0fb852d863039740e9f2c3406467e899
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692501"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a>Dynamics 365 Commerce 和 Microsoft Teams 集成常见问题解答

[!include [banner](includes/banner.md)]

本主题提供对有关 Microsoft Dynamics 365 Commerce 和 Microsoft Teams 集成的常见问题的解答。

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a>当从 Commerce 预配 Teams 时，商店中的谁将成为团队的负责人？ 

所有商店经理都将作为负责人自动添加到相应的团队组中，以便他们可以执行诸如添加专有渠道以及添加或删除成员的操作。 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a>如何在 Commerce Headquarters 中向员工分配“通信经理”角色？ 

Microsoft Teams 中的通信经理能够创建和发布任务列表。 需要成为通信经理的组织员工必须在 Commerce Headquarters 中向他们分配了“零售任务经理”角色。

若要在 Commerce Headquarters 中向员工分配零售任务经理角色，请按照下列步骤操作。

1. 转到 **Retail 和 Commerce \> 员工 \> 用户**。
1. 选择某一员工。
1. 在 **用户的角色** 快速选项卡，选择 **分配角色**。
1. 在 **将角色分配给用户** 对话框中，选择 **零售任务经理** 角色，然后选择 **确定**。

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a>如何使特定的组织层次结构可上传到 Microsoft Teams 中？

在 Commerce Headquarters 中，每个组织的层次结构都关联了一个或多个目的。 确保要预配到 Microsoft Teams 中的层次结构有与之关联的 **零售报告** 目的，如以下示例图像所示。 

![Commerce Headquarters 中组织层次结构目的示例。](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a>如何使零售商店工作人员使用 Azure Active Directory (Azure AD) 登录到 Commerce 销售点 (POS)？

有关如何将 Commerce POS 登录体验配置为使用 Azure AD 身份验证的信息，请参阅[为 POS 登录启用 Azure Active Directory 身份验证](aad-pos-logon.md)。

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a>如果我的组织已在 Microsoft Teams 中创建团队，如何在 Commerce Headquarters 中映射商店和相应的团队？

有关在有预先存在的团队的情况下如何映射商店和团队的信息，请参阅[如果您的组织在 Microsoft Teams 中有预先存在的团队，请映射商店和相应的团队](map-stores-existing-teams.md)。

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a>如何清除会话存储中存储的 Microsoft Graph API 令牌？

使用 Azure Active Directory (Azure AD) 帐户登录到销售点 (POS) 的用户应从 POS 注销或关闭应用程序以清除会话存储。 

> [!TIP]
> 建议的最佳做法是始终让商店工作人员锁定 POS 终端或在不使用终端时从会话中注销。 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a>如果商店没有商店经理，会发生什么情况？

如果商店没有经理，将不会为商店或在 Teams 中创建团队组。 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a>如果商店经理离开公司，会发生什么情况？

具有负责人角色的任何人都可以在 Commerce Headquarters 中添加新的商店经理，并重新预配 Teams，以便新经理在 Teams 中具有对组的必要特权。 

## <a name="additional-resources"></a>其他资源

[Dynamics 365 Commerce 和 Microsoft Teams 集成概览](commerce-teams-integration.md)

[启用 Dynamics 365 Commerce 和 Microsoft Teams 集成](enable-teams-integration.md)

[从 Dynamics 365 Commerce 预配 Microsoft Teams](provision-teams-from-commerce.md)

[在 Microsoft Teams 和 Dynamics 365 Commerce POS 之间同步任务管理](synchronize-tasks-teams-pos.md)

[在 Microsoft Teams 中管理用户角色](manage-user-roles-teams.md)

[如果 Microsoft Teams 中有预先存在的团队，映射商店和团队](map-stores-existing-teams.md)
