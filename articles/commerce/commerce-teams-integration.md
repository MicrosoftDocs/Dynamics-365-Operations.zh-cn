---
title: Dynamics 365 Commerce 和 Microsoft Teams 集成概览
description: 本主题介绍了 Microsoft Dynamics 365 Commerce 和 Microsoft Teams 集成的概览。
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6d82c1cafe35db5523c58870f4dcb2a7f63134a1
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352630"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a>Dynamics 365 Commerce 和 Microsoft Teams 集成概览

[!include [banner](includes/banner.md)]

本主题介绍了 Microsoft Dynamics 365 Commerce 和 Microsoft Teams 集成的概览。

Dynamics 365 Commerce 将与 Teams 集成，以通过同步两个应用程序之间的任务管理来帮助客户及其员工提供工作效率。 Commerce 和 Teams 集成提供的无缝任务管理使商店经理和员工可以创建任务列表，将任务分配到多个商店，并从任一应用程序跟踪跨商店的任务状态。

Commerce 和 Teams 集成从 Commerce 版本 10.0.18 版本开始可用。

## <a name="key-features"></a>主要功能

以下是 Commerce 和 Microsoft Teams 集成提供的一些关键功能：

- 通过利用 Commerce 中明确定义的信息（例如组织结构和有关商店、工作人员、权限和业务环境的信息）预配 Teams。
- 在 Commerce 和 Teams 之间轻松同步正在进行的更改（例如，添加新商店或雇用新员工），但保持 Commerce 为组织结构数据的主要来源。
- 在 Commerce 和 Teams 之间集成任务管理，以帮助商店工作人员、商店经理、区域经理和通信经理从任一应用程序处理任务管理。

## <a name="prerequisites-for-using-integration-features"></a>使用集成功能的先决条件

必须先满足以下先决条件，然后才能开始使用 Microsoft Teams 集成功能：

- Microsoft 365 商业版标准许可证（此许可证包括 Teams。）
- 适用于所有商店经理和工作人员的 Azure Active Directory (Azure AD) 帐户
- 使用 Azure AD 身份验证配置的销售点 (POS) 系统

## <a name="conceptual-architecture"></a>概念体系结构

下图显示 Dynamics 365 Commerce 和 Microsoft Teams 集成的概念体系结构，以旧金山商店为例。 Teams 和 Commerce POS 应用程序使用 Microsoft Planner 作为存储库，以便从 Teams 发布的任务显示在 POS 应用程序中，而由商店经理在 POS 应用程序中创建的临时任务显示在 Teams 中，从而在应用程序之间提供无缝的任务管理体验。    

![Commerce 和 Teams 集成的体系结构。](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a>其他资源

[启用 Dynamics 365 Commerce 和 Microsoft Teams 集成](enable-teams-integration.md)

[从 Dynamics 365 Commerce 预配 Microsoft Teams](provision-teams-from-commerce.md)

[在 Microsoft Teams 和 Dynamics 365 Commerce POS 之间同步任务管理](synchronize-tasks-teams-pos.md)

[在 Microsoft Teams 中管理用户角色](manage-user-roles-teams.md)

[如果 Microsoft Teams 中有预先存在的团队，映射商店和团队](map-stores-existing-teams.md)

[Dynamics 365 Commerce 和 Microsoft Teams 集成常见问题解答](teams-integration-faq.md)
