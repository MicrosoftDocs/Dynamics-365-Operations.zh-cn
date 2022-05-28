---
title: 在 Microsoft Teams 和 Dynamics 365 Commerce POS 之间同步任务管理
description: 本主题介绍如何在 Microsoft Teams 和 Dynamics 365 Commerce 销售点 (POS) 之间同步任务管理。
author: gvrmohanreddy
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b7bb38a415524290d1636eda1f379f3cdcf7e593
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688903"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>在 Microsoft Teams 和 Dynamics 365 Commerce POS 之间同步任务管理

[!include [banner](includes/banner.md)]

本主题介绍如何在 Microsoft Teams 和 Dynamics 365 Commerce 销售点 (POS) 之间同步任务管理。

Teams 集成的主要目的之一是在 POS 应用程序和 Teams 之间同步任务管理。 这样，商店员工可以使用 POS 应用程序或 Teams 来管理任务，而不必切换应用程序。

由于 Planner 用作 Teams 中任务的存储库，因此 Teams 和 Dynamics 365 Commerce 之间必须存在链接。 通过使用给定商店团队的特定计划 ID 来建立此链接。

以下过程显示了如何在 POS 和 Teams 应用程序之间设置任务管理同步。

## <a name="publish-a-test-task-list-in-teams"></a>在 Teams 中发布测试任务列表

以下过程假设您的商店团队首次使用与 Commerce 的 Microsoft Teams 任务管理集成。

若要在 Teams 中发布测试任务列表，请按照下列步骤操作。

1. 以通信经理身份登录到 Teams。 通常，通信经理是在 Commerce 中具有 **区域经理** 角色的用户。
1. 在左侧导航窗格中，选择 **按 Planner 划分的任务**。
1. 在 **已发布列表** 选项卡上，选择左下角的 **新建列表**，然后将新列表命名为 **测试任务列表**。
1. 选择 **创建**。 新列表将显示在 **草稿** 下。
1. 在 **任务标题** 下，向第一个任务提供标题 **测试 Teams 集成**。 然后选择 **输入**。
1. 在 **草稿** 列表中，选择任务列表。 然后，选择右上角的 **发布** 。
1. 在 **选择要发布给的人** 对话框中，选择应该接收测试任务列表的团队。
1. 选择 **下一步** 以查看您的发布计划。 如果必须进行更改，请选择 **后退**。 
1. 选择 **确认继续**，然后选择 **发布**。
1. 发布完成后，**已发布列表** 选项卡顶部的消息指示您的任务列表是否已成功交付。

有关详细信息，请参阅[发布任务列表以创建和跟踪组织中的工作](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df)。

## <a name="link-pos-and-teams-for-task-management"></a>链接 POS 和 Teams 以进行任务管理

若要在 Commerce Headquarters 中链接 POS 和 Microsoft Teams 应用程序以进行任务管理，请按照下列步骤操作。

> [!NOTE]
> 在尝试将任务管理与 Microsoft Teams 集成之前，请确保您已启用 [Dynamics 365 Commerce 和 Microsoft Teams 集成](enable-teams-integration.md)。 

1. 转到 **Retail 和 Commerce \> 任务管理 \> 与 Microsoft Teams 的任务集成**。
1. 在操作窗格上，选择 **编辑**。
1. 将 **启用任务管理集成** 选项设置为 **是**。
1. 在操作窗格上，选择 **保存**。
1. 在操作窗格上，选择 **设置任务管理**。 您应该收到一条通知，指示将创建名为 **Teams 预配** 的批处理作业。
1. 转到 **系统管理 \> 查询 \> 批处理作业**，查找具有描述 **Teams 预配** 的最新作业。 等待此作业完成运行。
1. 运行 **CDX 作业 1070** 以将计划 ID 和商店引用发布到 Retail Server。

## <a name="additional-resources"></a>其他资源

[Dynamics 365 Commerce 和 Microsoft Teams 集成概览](commerce-teams-integration.md)

[启用 Dynamics 365 Commerce 和 Microsoft Teams 集成](enable-teams-integration.md)

[从 Dynamics 365 Commerce 预配 Microsoft Teams](provision-teams-from-commerce.md)

[在 Microsoft Teams 中管理用户角色](manage-user-roles-teams.md)

[如果 Microsoft Teams 中有预先存在的团队，映射商店和团队](map-stores-existing-teams.md)

[Dynamics 365 Commerce 和 Microsoft Teams 集成常见问题解答](teams-integration-faq.md)
