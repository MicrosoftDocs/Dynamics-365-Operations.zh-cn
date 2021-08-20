---
title: 如果 Microsoft Teams 中有预先存在的团队，映射商店和团队
description: 本主题介绍如果您的组织在 Commerce 集成之前已在 Microsoft Teams 中创建了团队，如何在 Dynamics 365 Commerce Headquarters 中映射商店和相应的团队。
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6faba58304e1fe9e9ba2ce1a76fbf1cc783466bf01b0d4e3774e8ed090485bb1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757361"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a>如果 Microsoft Teams 中有预先存在的团队，映射商店和团队

[!include [banner](includes/banner.md)]

本主题介绍如果您的组织在 Commerce 集成之前已在 Microsoft Teams 中创建了团队，如何在 Dynamics 365 Commerce Headquarters 中映射商店和相应的团队。

在集成 Dynamics 365 Commerce 和 Microsoft Teams 之前，您的组织可能已为部分或全部商店创建了团队。 如果是这种情况，若要在 Commerce POS 和 Microsoft Teams 之间建立任务同步，您必须提供 Commerce Headquarters 中商店和相应团队的映射。

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a>在 Commerce Headquarters 中映射商店和相应的团队 

若要在 Commerce Headquarters 中映射商店和相应的团队，请按照下列步骤操作。

1. 转到 **系统管理 \> 工作区 \> 数据管理**。
1. 选择 **导出**。 
1. 在操作窗格上，选择 **新建**。
1. 在 **组名称** 下，输入“导出 Teams 映射”。
1. 在 **选定实体** 快速选项卡上，选择 **添加实体**。 将显示 **添加实体** 对话框。  
1. 在 **实体名称** 下拉列表中，选择 **源与团队之间的 Teams 映射**。
1. 在 **目标数据格式** 下拉列表中，选择 **CSV**。
1. 选择 **添加**，然后选择 **关闭**。
1. 在操作窗格下的左上角，选择 **立即导出**。
1. 在 **实体处理状态** 下，选择 **下载文件**。
1. 在导出的 CSV 文件中，输入 **SOURCETYPE**、**SOURCEID** 和 **TEAMID** 的值，如下所示：
    - 对于 **SOURCETYPE**，输入“RetailStore”。 
    - 对于 **SOURCEID**，输入商店编号（例如，针对旧金山商店输入“000135”）。 您可以在 **Retail 和 Commerce \> 渠道 \> 商店** 中找到商店编号。
    - 对于 **TEAMID**，输入 Microsoft Teams 中相应的团队 ID（例如，“5f8bc92b-6aa8-451e-85d1-3949c01ddc6c”）。 您可以在 [admin.teams.microsoft.com](https://admin.teams.microsoft.com) 中找到团队 ID 信息。
1. 将 CSV 文件保存到本地计算机。
1. 转到 **系统管理 \> 工作区 \> 数据管理**，然后选择 **导入**。
1. 在 **选定实体** 快速选项卡上，选择 **添加文件**。 将显示 **添加文件** 对话框。
1. 在 **实体名称** 下拉列表中，选择 **源与团队之间的 Teams 映射**。
1. 在 **源数据格式** 下拉列表中，选择 **CSV**。
1. 选择 **上传和添加**，选择之前保存的 CSV 文件，然后选择 **打开**。
1. 在 **添加文件** 对话框中，选择 **关闭**。
1. 在操作窗格上，选择 **保存**，然后选择 **导入**。

以下示例图像显示了 Commerce 中的 **导出 Teams 映射** 组，其中具有 **添加实体** 元素并且导出的 CSV 文件标题突出显示。

![Commerce 中的导出 Teams 映射组，突出显示了添加实体元素和导出的 CSV 文件标题。](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> 完成上述步骤后，请按照[在 Microsoft Teams 和 POS 之间同步任务管理](synchronize-tasks-teams-pos.md)中的步骤同步任务管理。 

## <a name="additional-resources"></a>其他资源

[Dynamics 365 Commerce 和 Microsoft Teams 集成概览](commerce-teams-integration.md)

[启用 Dynamics 365 Commerce 和 Microsoft Teams 集成](enable-teams-integration.md)

[从 Dynamics 365 Commerce 预配 Microsoft Teams](provision-teams-from-commerce.md)

[在 Microsoft Teams 和 Dynamics 365 Commerce POS 之间同步任务管理](synchronize-tasks-teams-pos.md)

[在 Microsoft Teams 中管理用户角色](manage-user-roles-teams.md)

[Dynamics 365 Commerce 和 Microsoft Teams 集成常见问题解答](teams-integration-faq.md)
