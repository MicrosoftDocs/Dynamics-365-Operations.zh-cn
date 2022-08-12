---
title: 创建从 Human Resources 到其他环境的链接
description: 本文介绍如何创建从 Microsoft Dynamics 365 Human Resources 到其他 Dynamics 365 环境的链接。
author: twheeloc
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9640f460ed7b0b1a0cfdffb7c318bf833f8627fc
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065284"
---
# <a name="create-links-from-human-resources-to-another-finance-environment"></a>创建从 Human Resources 到 Finance 环境的链接

客户可能有两个正在使用的 Dynamics 365 环境。 例如，客户在 Finance 基础结构中可能有一个 Dynamics 365 Human Resources 环境，并且需要连接到其他 Dynamics 365 Finance 环境。 

此功能将允许从 Human Resources 页面链接到另一个 Finance 环境中的特定页面。 配置链接后，您可以指定在 Human Resources 中提供链接的位置，以及将在其他环境中打开的目标页面。

> [!Note] 
> 您必须在 **功能管理** 中开启 **Human Resources 用户体验增强** 才能获得此功能。

## <a name="configure-target-systems"></a>配置目标系统

在 Human Resources 中，系统管理员可以定义将在 **Human Resources** 页面上显示的链接。 配置的一部分是您希望作为链接目标导航到的 Finance 环境。 

要配置目标系统，请执行以下操作：
1. 在 **配置链接** 页面上，选择 **配置目标系统**。  
2. 输入目标系统名称并提供 Finance 环境的 URL。 在配置您的目标系统后，您可以定义您的链接。

## <a name="configure-links"></a>配置链接

创建的每个链接将定义了以下信息：
 - **链接**：链接的名称。 仅用于标识。
 - **启用此链接**：如果要向 Human Resources 用户显示链接，请设置为 **是**。
 - **显示名称**：输入将显示为辅助环境链接的名称。 
 - **窗体上的表面链接**：选择您希望显示链接的页面。 链接只能显示在 **员工自助服务** 工作区以及 **工作**、**职位**、**工作人员** 和 **简化的工作人员** 页面上。
 - **组**：您可以使用组来组织链接。 选择现有组或使用 **组** 列创建新组。
 - **目标系统**：选择使用 **配置目标系统** 选项创建的目标系统。 这将是在使用链接导航时使用的次要环境。
 - **使用用户的当前公司**：选择 **是** 以在导航到 Finance 时使用用户的当前公司。 选择 **否** 可以选择应使用的公司。
 - **目标** 菜单项：输入导航时链接应使用的 Finance 环境中的菜单项。 提供您可以直接导航的菜单项。 

   要查找所需的菜单项，请执行以下操作：
   1. 转到 Finance 环境并打开作为导航目标的页面。 
   2. 从 URL 复制菜单项。 例如，如果您希望链接将您带到财务和运营中的员工列表，请输入在 URL 中的 "&mi" 后出现的值。 
   3. 在本示例中导航到员工列表页面的菜单项是：HcmWorkerListPage_Employees。

 - **链接到数据源**：选择链接所引用数据的源。 提供最常见的源，如 **工作人员** 和 **职位**。

### <a name="access-to-links"></a>访问链接

系统管理员将在定义的页面上看到新创建的链接，即使 **启用此链接** 选项设置为 **否**。 这可以用于在向其他员工显示链接前对链接进行测试。 在 **启用此链接** 选项设置为 **是** 后，所有其他角色将只能看到配置的链接。 有权访问链接显示页面的员工将有权访问这些链接。

用户还必须在定义的辅助环境中具有安全权限，才能访问该环境中的页面。 如果未定义，在使用链接时将显示安全对话框。


