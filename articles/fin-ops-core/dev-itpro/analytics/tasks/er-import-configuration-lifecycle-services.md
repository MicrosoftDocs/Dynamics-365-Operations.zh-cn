---
title: 从 Lifecycle Services 导入配置
description: 本主题介绍如何从 Microsoft Dynamics Lifecycle Services (LCS) 导入电子报告 (ER) 配置的新版本。
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 602886b0dd729b8ec52940f42bd1c393dac8acda
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093687"
---
# <a name="import-a-configuration-from-lifecycle-services"></a>从 Lifecycle Services 导入配置

[!include [banner](../../includes/banner.md)]

此主题介绍系统管理员或电子报表开发人员角色的用户如何从 Microsoft Dynamics Lifecycle Services (LCS) 中的[项目级资产库](../../lifecycle-services/asset-library.md)导入新[电子申报 (ER) 配置](../general-electronic-reporting.md#Configuration)版本。

在此示例中，您将为名称为 Litware, Inc. 的示例公司选择所需的 ER 配置版本并将其导入。这些步骤可以在任何公司完成，因为这些公司共享 ER 配置。 为了完成这些步骤，您必须首先完成[将配置上载到 Lifecycle Services](er-upload-configuration-into-lifecycle-services.md) 中的步骤。 还需要 LCS 的访问权限。

1. 通过使用以下角色之一登录到应用程序：

    - 电子申报开发人员
    - 系统管理员

2. 转到 **组织管理** \> **工作区** \> **电子申报**。
3. 选择 **配置**。

<a name="accessconditions"></a>
> [!NOTE]
> 确保当前 Dynamics 365 Finance 用户是其中包含用户希望[访问](../../lifecycle-services/asset-library.md#asset-library-support)来导入 ER 配置的资产库的 LCS 项目的成员。
>
> 不能从提供的域与 Finance 中使用的域不同的 ER 存储库访问 LCS 项目。 如果尝试访问，将显示空的 LCS 项目列表，并且您不能从 LCS 中的项目级资产库导入 ER 配置。 若要从用于导入 ER 配置的 ER 存储库访问项目级资产库，请使用属于为其预配了当前 Finance 实例的租户（域）的用户的凭证登录 Finance。

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a>删除数据模型配置的共享版本

1. 在 **配置** 页上的配置树中，选择 **示例模型配置**。

    在完成[将配置上载到 Lifecycle Services](er-upload-configuration-into-lifecycle-services.md) 中的步骤时，创建了示例数据模型配置的第一个版本并发布到了 LCS。 在此过程中，您将删除 ER 配置的这一版本。 然后将在本主题后文从 LCS 导入该版本。

2. 在列表中，找到并选择所需记录。

    对于此示例，请选择状态为 **已共享** 的配置版本。 此状态指示配置已发布到为 LCS。

3. 选择 **更改状态**。
4. 选择 **中断**。

    通过将所选版本的状态从 **已共享** 更改为 **已中断**，使此版本可删除。

5. 选择 **确定**。
6. 在列表中，找到并选择所需记录。

    对于此示例，请选择状态为 **中断** 的配置版本。

7. 选择 **删除**。
8. 选择 **是**。

    请注意，仅所选数据模型配置的草稿版本 2 现在可用。

9. 关闭该页面。

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a>从 LCS 导入数据模型配置的共享版本

1. 转到 **组织管理 \> 工作区 \> 电子申报**。

2. 在 **配置提供程序** 部分中，选择 **Litware, Inc.** 磁贴。

3. 在 **Litware, Inc.** 磁贴上，选择 **存储库**。

    现在可以打开 Litware, Inc 配置提供程序的存储库列表。

4. 选择 **打开**。

    对于此示例，请选择 **LCS** 存储库，然后打开。 必须具有该 LCS 项目和所选 ER 存储库访问的资产库的[访问权限](#accessconditions)。

5. 在列表中，标记所选的行。

    对于此示例，请在版本列表中选择 **示例模型配置** 的第一个版本。

6. 选择 **导入**。
7. 选择 **是** 确认从 LCS 导入所选版本。

    将通过参考消息确认已成功导入了所选版本。

8. 关闭该页面。
9. 关闭该页面。
10. 选择 **配置**。
11. 在树结构中，选择 **示例模型配置**。
12. 在列表中，找到并选择所需记录。

    对于此示例，请选择状态为 **已共享** 的配置版本。

    请注意，所选数据模型配置的共享版本 1 现在也可用。
