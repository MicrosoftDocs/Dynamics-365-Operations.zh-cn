---
title: 设置资产管理移动工作区
description: 本主题介绍如何设置 Microsoft Dynamics 365 Supply Chain Management 和 Finance and Operations (Dynamics 365) 移动应用以运行资产管理移动工作区，工作人员可以使用该工作区来执行资产管理任务。
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: bc170df2fc58ae6b42fbc8834caad0bb7cd16f69
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837769"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a>设置资产管理移动工作区

[!include [banner](../includes/banner.md)]

本主题介绍如何设置 Microsoft Dynamics 365 Supply Chain Management 和 Finance and Operations (Dynamics 365) 移动应用以运行 **资产管理** 移动工作区，工作人员可以使用该工作区来执行资产管理任务。

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a>在 Supply Chain Management 中设置维护工人用户

对于需要访问 **资产管理** 移动工作区的每个用户，请按照以下步骤操作。

1. 在 Supply Chain Management 中，转到 **人力资源 \> 工作人员**，确保要设置的用户存在工作人员记录。 根据需要创建新的工作人员记录。
1. 转到 **资产管理 \> 设置 \> 工作人员 \> 工作人员**，确保您在上一步中确定（或创建）的工作人员记录已映射到维护工人记录。 根据需要创建新的维护工人记录，然后将 **工作人员** 字段设置为上一步中的工作人员记录。
1. 转到 **资产管理 \> 设置 \> 工作人员 \> 维护工人组**，确保您在上一步中确定（或创建）的维护工人记录属于该维护工人组。
1. 转到 **系统管理 \> 用户**。
1. 在网格中选择相关用户。
1. 在 **用户详细信息** 快速选项卡上，将 **人员** 字段设置为您要与当前用户帐户关联的工作人员帐户。 此工作人员帐户应该是您在步骤 1 中确定（或创建）并在步骤 2 中映射到维护工人记录的工作人员记录。

> [!NOTE]
> 用户权限和安全角色应用于 **资产管理** 移动工作区的功能，就像它们会应用于 Supply Chain Management 用户界面的功能一样。 因此，您设置为访问 **资产管理** 移动工作区的每个用户必须具有直接在 Supply Chain Management 中直接执行类似操作所需的安全角色。

## <a name="publish-the-asset-management-mobile-workspace"></a>发布资产管理移动工作区

若要使资产管理功能在 Finance and Operations (Dynamics 365) 移动应用中可用，您必须发布 **资产管理** 移动工作区。

1. 在 Supply Chain Management 中，选择 **设置** 按钮（右上角的齿轮符号），然后在菜单上选择 **移动应用**。
1. 在 **管理移动应用** 对话框中，找到 **资产管理** 磁贴。 如果它包含文本“在元数据中 - 未发布”，说明该工作区尚未发布。 如果它包含文本“在元数据中 - 已发布”，说明工作区已发布，您可以跳过此过程的其余部分。

    ![管理移动应用对话框](media/mobile-workspaces.png "管理移动应用对话框")

1. 选择 **资产管理** 磁贴，然后在工具栏上选择 **发布**。 几秒钟后，您应该收到一条通知，说明工作区已成功发布。 此外，磁贴上的文本应会变为“在元数据中 - 已发布”。

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a>安装和设置 Finance and Operations (Dynamics 365) 移动应用

1. 转到以下应用商店之一，在移动设备上安装 **Microsoft Finance and Operations (Dynamics 365)** 应用：

    - [对于 Google Android 设备](https://go.microsoft.com/fwlink/?linkid=850662)
    - [对于 Apple iOS 设备](https://go.microsoft.com/fwlink/?linkid=850663)

1. 打开 Finance and Operations (Dynamics 365) 应用。 登录页面应会出现。 在 **登录** 字段中，输入您的 Supply Chain Management URL，或在 **最近环境** 列表中选择一个最近的 URL，然后点击 **连接**。

    ![登录页](media/mobile-app-sign-in.png "登录页")

1. 如果系统提示您确认连接，请选中 **我知道** 复选框，然后点击 **连接**。
1. 在 **选择帐户** 页上，使用您的 Microsoft 帐户登录到移动应用程序。

    **工作区** 页将显示。 其中将列出您的 Supply Chain Management 实例已发布的每个移动工作区。

    ![工作区列表](media/mobile-app-workspaces.png "工作区列表")

1. 如果必须更改法人（公司），请点击左上角的菜单按钮（有时称为汉堡包或汉堡包按钮），然后点击 **更改公司**。

    ![更改法人](media/mobile-app-change-comp.png "更改法人")

1. 在 **工作区** 页上，选择要使用的工作区将其打开。

    ![资产管理移动工作区](media/mobile-app-asset-workspace.png "资产管理移动工作区")

## <a name="work-with-the-asset-management-mobile-workspace"></a>使用资产管理移动工作区

有关如何使用 **资产管理** 移动工作区的详细信息，请参阅[使用资产管理移动工作区](asset-management-mobile-workspace.md)。

有关 Finance and Operations (Dynamics 365) 移动应用的详细信息，请参阅[移动应用主页](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]