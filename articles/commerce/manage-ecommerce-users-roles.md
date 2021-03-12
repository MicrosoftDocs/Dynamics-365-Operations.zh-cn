---
title: 管理电子商务用户和角色
description: 此主题介绍如何为用户授予 Microsoft Dynamics 365 Commerce 站点创作环境的访问权限。
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8d4987a824b786401c41c6ae63c8486ce7eb0c5d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995683"
---
# <a name="manage-e-commerce-users-and-roles"></a>管理电子商务用户和角色


[!include [banner](includes/banner.md)]

此主题介绍如何为用户授予 Microsoft Dynamics 365 Commerce 站点创作环境的访问权限。

为了帮助控制用户访问和授予用户执行特定任务的权限，站点制作环境使用您在 Microsoft Azure Active Directory (Azure AD) 中创建的安全组。 您首先从 Azure AD 将新的或现有的安全组分配给创作环境中的每位角色。 然后为单个用户授予权限或撤消其权限，方法是将这些用户添加到相应安全组，或从安全组删除这些用户。

## <a name="overview-of-roles-in-the-authoring-environment"></a>创作环境中的角色概述

Dynamics 365 for Commerce 创作环境支持以下角色。

| 角色                 | 说明 |
|----------------------|-------------|
| 系统管理员 | 具有此角色的用户拥有所有工具和所有评分和评价的所有权限。 还可以创建站点。 |
| 管理员   | 具有此角色的用户拥有特定站点结构中所有工具和 RnR 的所有权限。 |
| Web 制作者         | 具有此角色的用户可以创建页面、片段和模板，上传和管理资产，以及扩充产品和类别。 |
| 读者               | 具有此角色的用户可查看页面、模板、资产、片段、布局和设置，但是不能进行更改。 |
| RnR 审查者        | 具有此角色的用户可以审查产品评价。 |

## <a name="system-administrator-role"></a>系统管理员角色

在 Microsoft Dynamics Lifecycle Services (LCS) 环境中预配 Dynamics 365 Commerce 时，系统会请您为 **系统管理员** 角色提供安全组。 然后将此角色自动应用于您在正在配置的环境中创建的所有站点。 只能在 LCS 中更新此角色的安全组。 在所有站点的 **站点管理** 页中，其显示为只读，仅供参考。

## <a name="administrator-role"></a>管理员角色

在 Commerce 中创建新站点时，系统将请您为 **管理员** 角色提供安全组。 有关此角色授予的权限的概述，请参见本主题前文的表。

## <a name="add-or-update-security-groups"></a>添加或更新安全组

创建站点之后，只有与 **系统管理员** 和 **管理员** 角色关联的安全组中的用户才能访问该站点的创作环境。 若要为 **Web 制作者**、**RnR 审查者** 和 **读者** 角色分配用户，必须为这些角色分配安全组。 若要向角色添加安全组或更新当前分配给角色的安全组，请执行以下步骤。

1. 转到要更新的站点。
1. 在 **站点管理** 中，打开 **安全** 页。
1. 选择要修改的角色。
1. 向角色添加安全组，或从角色中删除安全组。

## <a name="additional-resources"></a>其他资源

[将脚本代码添加到站点页面以支持遥测](add-telemetry.md)

[站点的搜索引擎优化 (SEO) 注意事项](search-engine-optimization-considerations.md)

[管理内容安全策略 (CSP)](manage-csp.md)
