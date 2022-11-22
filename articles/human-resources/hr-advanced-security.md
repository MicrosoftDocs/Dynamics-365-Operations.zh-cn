---
title: 按照法人限制对工作人员的访问权限
description: 本文介绍如何按法人设置工作人员访问权限。
author: twheeloc
ms.date: 11/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fadd2c34d31bbd259255596c06a8e7517f7a774b
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780385"
---
# <a name="restrict-access-to-workers-by-legal-entity"></a>按照法人限制对工作人员的访问权限

本文介绍如何按法人设置工作人员访问权限。

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

员工受雇于法人。 下面举了一些示例加以说明：

- Aaron Con 受雇于 USSI 法人。
- Ahmed Barnett 受雇于 USMF 法人。
- Alicia Thornber 受雇于 GLSI 和 USMF 法人。

根据用户在公司中的角色，他们可能需要访问权限来查看所有法人的所有员工。 或者，可能必须对用户加以限制，让他们只能查看他们有权访问的法人的员工。 要控制用户可以查看哪些员工，在 **人力资源共享参数** 页面选择 **Restrict access to worker information** 参数。

例如，用户有权访问 **工作人员** 页面，且只有权访问 USMF 法人。 在这种情况下，用户可以查看上述列表中员工的以下信息：

- 如果未启用限制访问工作人员信息的功能，用户可以查看 Aaron、Ahmed 和 Alicia 的信息。
- 如果启用了此功能，用户只能查看 Alicia 和 Ahmed 的信息，因为他们还受雇于 USMF 法人。

显示的信息因您使用的应用程序而异。

## <a name="dynamics-365-human-resources-stand-alone"></a>Dynamics 365 Human Resources 独立

如果启用限制访问工作人员信息的功能，受限用户将在某些包含工作人员姓名的列表中看到空白值。

例如，只有权访问 USMF 法人的用户将遇到以下行为：

- 在 **有效职位** 列表中，**工作人员** 列对于 Aaron 的职位的将为空，因为用户无权访问 USSI 法人的员工。
- 如果用户向下钻取工作人员的姓名，会出现一个空白的 **工作人员** 页面。

## <a name="dynamics-365-human-resources-on-finance-infrastructure"></a>Finance 基础结构上的 Dynamics 365 Human Resources

如果启用限制访问工作人员信息的功能，受限用户将在某些列表中看到工作人员的姓名。

例如，只有权访问 USMF 法人的用户将遇到以下行为：

- 在 **有效职位** 列表中，**工作人员** 列将显示 Aaron 的姓名。 如果用户将鼠标悬停在工作人员的姓名上，将只显示姓名和职务。
- 如果用户向下钻取工作人员的姓名，会出现一个空白的 **工作人员** 页面。

> [!TIP]
> 如果您使用的是 Finance 基础结构上的 Dynamics 365 Human resources，您希望受限用户看到工作人员姓名是空白值，您可以在 **安全配置** 页面向用户角色添加 **限制对工作人员的访问** 安全权限。

启用此功能后，必须完成一些额外的步骤，来为视图必须受限的每个用户设置权限。

1. 在 **用户** 页面上，选择用户。
2. 选择用户的角色。 **分配组织** 选项变得可用。
3. 选择 **分配组织**。
4. 在新页面上，选择 **单独授予对特定组织的访问权限**，然后选择用户应有权访问的组织。
5. 对于用户拥有的每个其他角色（包括系统用户角色）重复步骤 2 到 4。

> [!NOTE]
> 用户有权访问的法人在所有用户角色之间必须一致。
