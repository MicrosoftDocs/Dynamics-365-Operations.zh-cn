---
title: Dynamics 365 Human Resources 基础结构合并已知问题
description: 本文列出了 Microsoft Dynamics 365 Human Resources 基础结构合并过程中可能出现的问题。
author: twheeloc
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3fe21df8be010ace3070ad08ed95f3d3efc7b01d
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838547"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-known-issues"></a>Dynamics 365 Human Resources 基础结构合并已知问题

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="shared-dataverse-environments"></a>共享 Dataverse 环境

双写入框架不支持将两个财务和运营应用环境链接到同一个 Dataverse 环境。 如果您有一个与以下两个项目共享的 Dataverse 环境，您必须复制 Dataverse 环境或将其拆分：

- 财务和运营应用
- 当前 Human Resources 环境

## <a name="environment-type-requirements"></a>环境类型要求

需要有以下环境类型，您才能够进行迁移：

- 如果您没有任何沙盒独立环境，必须创建一个来验证迁移。
- 如果您有多个生产独立环境，可以迁移其中一个。 请与 Microsoft 支持部门联系将其他环境标记为沙盒。

## <a name="teams-integration"></a>Teams 集成

Teams 中现有的 Human Resources 应用目前正在转移到 Microsoft Power Platform 解决方案。 有关详细信息，请参阅 [Teams 中的 Human Resources 应用](hr-admin-teams-leave-app.md)。

## <a name="dual-write-integration"></a>双写入集成

双重写入是一种现成基础结构，其提供 Customer Engagement 应用与财务和运营应用之间的近实时交互。 如果您的组织使用双重写入进行集成，您可能会受到所发现的一些问题的影响。 有关 Dataverse 表和问题的更多信息，请参阅 [Dataverse 表](hr-developer-entities.md)。

