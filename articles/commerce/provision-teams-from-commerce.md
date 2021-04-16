---
title: 从 Dynamics 365 Commerce 预配 Microsoft Teams
description: 本主题介绍如何使用组织数据从 Dynamics 365 Commerce 预配 Microsoft Teams。
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 96382c072e03506294d72899072a358091bda8ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842624"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a>从 Dynamics 365 Commerce 预配 Microsoft Teams

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

本主题介绍如何使用组织数据从 Dynamics 365 Commerce 预配 Microsoft Teams。

如果您尚未在此处为零售商店设置团队，Dynamics 365 Commerce 将提供一种轻松方式来预配 Teams。 通过利用 Commerce 中要在 Teams 中使用的明确定义的信息，您可以帮助商店员工开始使用 Teams。 此信息包括组织层次结构、商店名称、员工信息和 Azure Active Directory (Azure AD) 帐户。 

预配 Teams 的流程包括两个主要步骤：

1. 在 Teams 中，为每个零售商店创建团队，将商店工作人员添加为适当团队的成员。 如果一名员工与多个零售商店相关联，则团队成员身份将反映这一事实。 将创建包括区域经理作为成员的通信团队，以帮助从 Teams 发布任务。
1. 将您的组织层次结构从 Commerce 上传到 Teams。

## <a name="provision-teams-in-commerce-headquarters"></a>在 Commerce Headquarters 中预配 Teams

在预配 Microsoft Teams 之前，完成以下任务：

- 确认所有区域经理均已成为通信经理。
- 确认每个商店经理和工作人员的 Azure 帐户已与 Commerce Headquarters 中该经理或工作人员的工作人员记录相关联。

若要在 Commerce Headquarters 中预配 Teams，请按照下列步骤操作。

1. 转到 **Retail 和 Commerce \> 渠道设置 \> Microsoft Teams 集成配置**。
1. 在操作窗格上，选择 **预配团队**。 将创建名为 **Teams 预配** 的批处理作业。
1. 转到 **系统管理 \> 查询 \> 批处理作业**，查找具有描述 **Teams 预配** 的最新作业。 等待此作业完成运行。

> [!TIP]
> 如果您的区域经理、商店经理和商店工作人员均未与 Teams 许可证相关联，您可能会收到以下错误消息：“无法为用户检索适用的 Sku 类别。” 若要更正此问题，请在操作窗格上选择 **同步团队和成员**。

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a>在 Teams 管理中心中验证 Teams 预配

若要在 Microsoft Teams 管理中心中验证 Microsoft Teams 预配，请按照下列步骤操作。
    
1. 转到 [Teams 管理中心](https://admin.teams.microsoft.com/)，然后以您的电子商务租户的管理员身份登录。
1. 在左侧导航窗格中，选择 **Teams** 以展开它，然后选择 **管理团队**。
1. 确认已为每个 Commerce 零售商店创建了一个团队。
1. 选择团队，并确认已将商店工作人员作为成员添加到该团队。
1. 在左侧导航窗格中，选择 **用户**，并确认已将所有商店中的所有商店员工都添加为用户。

下图显示 Teams 管理中心中 **管理团队** 页面的示例。

![Teams 管理中心中“管理团队”页面的示例](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a>将 Commerce 组织层次结构上传到 Teams
    
Commerce 组织层次结构可在 Microsoft Teams 中使用，以将任务发布到使用相同层次结构的全部或选定商店。

若要将 Commerce 组织层次结构上传到 Teams，请按照下列步骤操作。
    
1. 在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> 渠道设置 \> Microsoft Teams 集成配置**。
1. 选择 **下载目标层次结构**，然后选择 **零售商店(按地区)** 以下载组织层次结构的以逗号分隔值 (CSV) 文件。
1. 通过按照[安装 Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install) 中的步骤安装 Microsoft Teams PowerShell 模块。
1. 当系统提示您位于 Teams PowerShell 窗口中时，使用 Azure AD 租户的管理员帐户登录。
1. 按照[设置团队目标层次结构](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy)中的步骤为目标层次结构上传 CSV 文件。

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a>验证组织层次结构是否已上传到 Teams

若要验证组织层次结构是否已上传到 Microsoft Teams，请按照下列步骤操作。

1. 以通信经理身份登录到 Teams。
1. 在左侧导航窗格中，选择 **按 Planner 划分的任务**。
1. 在 **已发布列表** 选项卡上，创建具有虚拟任务的新列表。
1. 选择 **发布**。 组织层次结构应显示在 **选择要发布给的人** 对话框中，如下图中的示例所示。

![“选择要发布给的人”对话框中的组织层次结构的示例](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a>其他资源

[Dynamics 365 Commerce 和 Microsoft Teams 集成概览](commerce-teams-integration.md)

[启用 Dynamics 365 Commerce 和 Microsoft Teams 集成](enable-teams-integration.md)

[在 Microsoft Teams 和 Dynamics 365 Commerce POS 之间同步任务管理](synchronize-tasks-teams-pos.md)

[在 Microsoft Teams 中管理用户角色](manage-user-roles-teams.md)

[如果 Microsoft Teams 中有预先存在的团队，映射商店和团队](map-stores-existing-teams.md)

[Dynamics 365 Commerce 和 Microsoft Teams 集成常见问题解答](teams-integration-faq.md)
