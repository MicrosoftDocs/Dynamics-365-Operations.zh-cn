---
title: Microsoft Project Client 集成
description: 规划和维护项目计划可能非常复杂，因此项目经理需要使用工具来帮助管理此任务。 与 Microsoft Project Client 的集成提供了对打开和管理项目工作分解结构的支持。
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 48feb0182c623714b2acffafc42016c0471ba6c1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556567"
---
# <a name="microsoft-project-client-integration"></a>Microsoft Project Client 集成

[!include [banner](../includes/banner.md)]

规划和维护项目计划可能非常复杂，因此项目经理需要使用工具来帮助管理此任务。 与 Microsoft Project Client 的集成提供了对打开和管理项目工作分解结构的支持。 项目经理可将任何更改发布回 Finance and Operations 项目工作分解结构。

> [!NOTE]
> 如果您在使用 Microsoft Dynamics 365 for Finance and Operations 7 月更新，您必须安装 KB 4054797 和 4055884。

## <a name="configure-the-microsoft-project-client-add-in"></a>配置 Microsoft Project Client 加载项
若要实现与 Microsoft Project Client 集成，需要在用户的客户端 Microsoft Project 应用程序中安装 Microsoft Dynamics 365 加载项。 方法是打开**项目管理工作区**。

•   单击该工作区的**链接** > **设置**部分中的**配置项目客户端加载项**。

•   单击**打开**，然后在系统提示时单击**运行**。

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>在 Microsoft Project Client 中打开和编辑现有草稿工作分解结构。
如果已为 Finance and Operations 中的某个项目创建了工作分解结构，并且该工作分解结构处于草稿状态，则可在 Microsoft Project Client 应用程序中打开该工作分解结构。 若要从**项目**页面打开，请单击**计划**选项卡中的**在 Microsoft Project 中打开**链接。也可以从 Microsoft Project Client 应用程序内部打开该页面，方法是单击 **Microsoft Dynamics 365** 选项卡中的**打开**。从列表中选择**法人**和**项目**。

> [!NOTE]
> 如果浏览器使用的是 Internet Explorer，则需要单击**保存**手动从文件下载到的位置打开。 或者，单击 **保存并打开**以在 Microsoft Project Client 中打开文件。 保存时，请勿重命名文件。

使用 Microsoft Project Client 对文件进行任何编辑之前，需要将其签出。单击 **Microsoft Dynamics 365** 选项卡中的**签出**。这将阻止其他用户在同一时间从 Finance and Operations 内部编辑此工作分解结构。 若要在完成任何编辑之后发布工作分解结构，请单击 **Microsoft Dynamics 365** 选项卡上的**签入**。

如果已在 Finance and Operations 中向项目添加了项目团队，将使用团队成员填充资源列表。 如果尚未向项目添加项目团队，可通过单击 **Microsoft Dynamics 365** 选项卡上的**资源**按钮，在 Microsoft Project Client 内部选择资源和建立团队。 

签入期间，将把以下数据同步回 Finance and Operations：

•   任务名称

•   开始日期

•   完成日期

•   前置任务

•   资源名称

•   类别

•   资源类别

•   工时

•   注释

•   优先级

> [!NOTE]
> 如果向 Microsoft Project Client 文件添加其他任何列，这些列将不会保存到该文件，也不会在再次打开该文件时显示。

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>使用 Microsoft Project Client 为现有项目创建工作分解结构
若要使用 Microsoft Project Client 为现有项目创建新的工作分解结构，请执行以下步骤：


1.  打开 Microsoft Project Client。

2.  在 **Microsoft Dynamics 365** 选项卡上，单击**打开**。

3.  选择项目的**法人**。

4.  选择**项目**。

5.  单击 **Microsoft Dynamics 365** 选项卡上的**签出**。

6.  准备好发布到 Finance and Operations 时，在 **Microsoft Dynamics 365** 选项卡上单击**签入**。

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>使用 Microsoft Project Client 替换现有项目的现有工作分解结构
若要使用 Microsoft Project Client 创建新工作分解结构和替换现有项目的现有工作分解结构，请执行以下步骤：

1.  打开 Microsoft Project Client。

2.  在 Microsoft Project Client 中创建计划。

3.  在 **Microsoft Dynamics 365** 选项卡上，单击**保存更改** > **替换现有项目**。

4.  选择项目的**法人**。

5.  选择**项目**。

6.  单击**确定**。

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>从 Microsoft Project Client 内部创建新项目


1.  打开 Microsoft Project Client。

2.  在 Microsoft Project Client 中创建计划。

3.  在 **Microsoft Dynamics 365** 选项卡上，单击**保存更改** > **保存到新项目**。

4.  选择项目的**法人**。

5.  必要时输入**项目 ID**。

6.  输入**项目名称**。

7.  选择**项目类型**、**项目组**和**项目合同 ID**。 也可以通过单击 **新建**创建新的项目合同。

8.  选择要用于安排资源的**日历**。

11. 单击**确定**。
