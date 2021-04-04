---
title: 配置任务管理
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中配置任务管理功能。
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ba2283bbfa2fdce75d3fbef6fcff47dd872c7998
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478036"
---
# <a name="configure-task-management"></a>配置任务管理

[!include [banner](includes/banner.md)]

本主题介绍如何在 Microsoft Dynamics 365 Commerce 中配置任务管理功能。

必须先配置任务管理，Dynamics 365 Commerce 经理和员工才能使用 Commerce 中的任务管理功能。 配置步骤包括为经理和员工授予权限，将权限分发给销售点 (POS) 客户端，设置 POS 通知，以及配置 POS 应用程序主页中的 **任务** 磁贴。

## <a name="configure-permissions-for-store-managers"></a>配置商店经理的权限

给定商店中的每位工作人员都可以查看为该商店分配的所有任务。 他们还可以更新为其分配的任务的状态。 但是，商店经理之类个人必须拥有管理权限，才能管理为商店分配的任务和创建单一目标任务。

若要为商店经理配置任务管理权限，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> 员工 \> 权限组**。
1. 选择特定权限组（例如，**经理**），然后选择 **编辑**。
1. 在 **权限** 快速选项卡上，将 **允许任务管理** 选项设置为 **是**。
1. 在 **通知** 快速选项卡上，添加 **任务管理** 操作，然后在 **显示顺序** 字段中输入值。 例如，如果 **订单履行** 操作的 **显示顺序** 值已经为 **1**，则输入 **2**。
    
> [!NOTE]
> 如果一位非经理人员必须在 POS 中具有任务管理权限，可以为该人授予权限。 也可以为非经理创建新的权限组，然后将 **允许任务管理** 选项设置为 **是**。

下图显示如何为商店经理配置任务管理权限。

![为商店经理配置任务管理权限](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a>为员工配置权限

员工必须有权创建任务列表，管理分配条件和配置任何任务列表的重复。 若要配置这些权限，请为员工分配 **零售任务经理** 角色。

若要为员工配置权限，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> 员工 \> 用户**。
1. 选择某一员工。
1. 在 **用户的角色** 快速选项卡，选择 **分配角色**。
1. 在 **将角色分配给用户** 对话框中，选择 **零售任务经理** 角色，然后选择 **确定**。

## <a name="distribute-permissions-to-pos-clients"></a>为 POS 客户端分配权限

必须先分发权限并同步到 POS 客户端，员工才能使用这些客户端。

若要为 POS 客户端分发权限，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。
1. 选择 **1060**（**员工**）分发计划，然后选择 **立即运行**。
1. 选择 **1070**（**渠道配置**）分发计划，然后选择 **立即运行**。

## <a name="configure-pos-notifications-for-tasks"></a>为任务配置 POS 通知

必须配置任务管理，以便 POS 应用程序中支持通知。

若要为任务配置 POS 通知，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS \> POS 操作**。
1. 找到操作 **1400**（**任务管理**），然后选中其 **启用通知** 复选框。

下图显示 **POS 操作** 页中的 **任务管理** 操作。

![POS 操作页中的任务管理操作](media/HQ-POS-Tasks-Notifications.png)

有关如何配置 POS 通知的详细信息，请参阅[在销售点 (POS) 中显示订单通知](notifications-pos.md)。

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a>配置 POS 应用程序主页中的“任务”磁贴

配置 POS 应用程序主页中的 **任务** 磁贴之前，请参阅[销售点 (POS) 的屏幕截图](pos-screen-layouts.md)以获取有关如何配置和将新按钮添加到 POS 屏幕布局的信息。

若要配置 POS 应用程序主页中的 **任务** 磁贴，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS \> 屏幕布局**。
1. 选择一个屏幕布局，选择布局大小，然后选择按钮网格。
1. 在 **按钮网格** 快速选项卡上，选择 **设计器** 编辑所选按钮网格。
1. 向主页的相应部分添加 **任务** 磁贴。

下图显示 POS 主页中的 **任务** 磁贴的示例。

![POS 主页上的“任务”磁贴](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a>其他资源

[任务管理概述](task-mgmt-overview.md)

[创建任务列表和添加任务](task-mgmt-create-lists.md)

[将任务列表分配给商店或员工](task-mgmt-assign-lists.md)

[POS 中的任务管理](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
