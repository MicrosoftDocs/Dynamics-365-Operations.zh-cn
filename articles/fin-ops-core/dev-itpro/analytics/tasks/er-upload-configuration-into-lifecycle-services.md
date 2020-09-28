---
title: 上载配置到 Lifecycle Services
description: 此主题介绍系统管理员或电子报表开发人员角色的用户如何新建电子申报 (ER) 配置并上载到 Microsoft Dynamics Lifecycle Services (LCS) 中。
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c43bad3ee2530a454de718a0a7da4d1e468a4af4
ms.sourcegitcommit: 9857d5cbdc0ab2fc9db049ac5ad118fc2b29bedc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/14/2020
ms.locfileid: "3810683"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a>上载配置到 Lifecycle Services

[!include [banner](../../includes/banner.md)]

此主题介绍系统管理员或电子报表开发人员角色的用户如何新建[电子申报 (ER) 配置](../general-electronic-reporting.md#Configuration)并上载到 Microsoft Dynamics Lifecycle Services (LCS) 中的[项目级资产库](../../lifecycle-services/asset-library.md)中。

此示例以名称为 Litware，Inc. 的示例公司为例，您将创建一个配置提供程序并将其上载到 LCS 中。这些步骤可在任何公司完成，因为公司之间共享 ER 配置。 为了完成这些步骤，您必须首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)中的步骤。 还需要 LCS 的访问权限。

1. 通过使用以下角色之一登录到应用程序：

    - 电子申报开发人员
    - 系统管理员

2. 转到**组织管理** \> **工作区** \> **电子申报**。
3. 选择 **Litware, Inc.** 并将其标记为**有效**。
4. 选择**配置**。

<a name="accessconditions"></a>
> [!NOTE]
> 确保当前 Dynamics 365 Finance 用户是其中包含用于导入 ER 配置的[资产库](../../lifecycle-services/asset-library.md#asset-library-support)的 LCS 项目的成员。
>
> 不能从提供的域与 Finance 中使用的域不同的 ER 存储库访问 LCS 项目。 如果尝试访问，将显示空的 LCS 项目列表，并且您不能从 LCS 中的项目级资产库导入 ER 配置。 若要从用于导入 ER 配置的 ER 存储库访问项目级资产库，请使用属于为其预配了当前 Finance 实例的租户（域）的用户的凭证登录 Finance。

## <a name="create-a-new-data-model-configuration"></a>创建新的数据模型配置

1. 转到**组织管理 \> 电子申报 \> 配置**。
2. 在**配置**页面中，选择**创建配置**，以打开下拉对话框。

    在此示例中，您将创建含有电子单据的示例数据模型的配置。 此数据模型配置稍后将上载到 LCS。

3. 在**名称**字段中，输入**示例模型配置**。
4. 在**描述**字段中，输入**示例模型配置**。
5. 选择**创建配置**。
6. 选择**模型设计器** 。
7. 选择**新建**。
8. 在**名称**字段中，输入**入口点**。
9. 选择**添加**。
10. 选择**保存**。
11. 关闭该页面。
12. 选择**更改状态**。
13. 选择**完成**。
14. 选择**确定**。
15. 关闭该页面。

## <a name="register-a-new-repository"></a>登记新存储库

1. 转到**组织管理 \> 工作区 \> 电子申报**。

2. 在**配置提供程序**部分中，选择 **Litware, Inc.** 磁贴。

3. 在 **Litware, Inc.** 磁贴上，选择**存储库**。

    现在可以打开 Litware, Inc 配置提供程序的存储库列表。

4. 选择**添加**以打开下拉对话框。

    现在可以添加新存储库。

5. 在**配置存储库类型**字段中，选择 **LCS**。
6. 选择**创建存储库**。
7. 在**项目**字段中，输入或选择一个值。

    在本示例中，选择所需 LCS 项目。 您必须有权[访问](#accessconditions)该项目。

8. 选择**确定**。

    完成新的存储库输入。

9. 在列表中，标记所选的行。

    对于此示例，请选择 **LCS** 存储库记录。

    请注意，当前提供商将标记注册的存储库。 换句话说，只能将该提供商负责的配置放入此存储库中，从而上载到所选 LCS 项目中。

10. 选择**打开**。

    打开存储库查看 ER 配置列表。 如果尚未将所选项目用于共享 ER 配置，列表将为空。

11. 关闭该页面。
12. 关闭该页面。

## <a name="upload-a-configuration-into-lcs"></a>将配置上传到 LCS 中

1. 转到**组织管理 \> 电子申报 \> 配置**。
2. 在**配置**页上的配置树中，选择**示例模型配置**。

    必须选择已完成的创建的配置。

3. 在列表中，找到并选择所需记录。

    对于此示例，请选择状态为**已完成**的所选配置版本。

4. 选择**更改状态**。
5. 选择**共享**。

    在 LCS 中发布配置时，配置的状态将从**已完成**变为**已共享**。

6. 选择**确定**。
7. 在列表中，找到并选择所需记录。

    对于此示例，请选择状态为**已共享**的配置版本。

    请注意，所选版本的状态已从**已完成**变为**已共享**。

8. 关闭该页面。
9. 选择**存储库**。

    现在可以打开 Litware, Inc 配置提供程序的存储库列表。

10. 选择**打开**。

    对于此示例，请选择 **LCS** 存储库，然后打开。

    请注意，所选配置显示为所选 LCS 项目的资产。

11. 通过转到 <https://lcs.dynamics.com> 打开 LCS。
12. 打开一个先前用于存储库注册的项目。
13. 打开项目的资产库。
14. 选择 **GER 配置**资产类型。

    应该会列出您上载的 ER 配置。

    请注意，如果提供程序有权访问此 LCS 项目，上载的 LCS 配置可以导入到其他实例中。
