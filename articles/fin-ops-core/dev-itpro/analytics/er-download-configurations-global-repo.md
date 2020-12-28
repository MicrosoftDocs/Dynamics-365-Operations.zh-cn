---
title: 从 Configuration service 的全局知识库下载 ER 配置
description: 本主题说明如何从 Configuration service 的全局知识库下载电子申报 (ER) 配置。
author: NickSelin
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a96e78a64fe0559ae5f3bfddabf3fe1cad8a3dcb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679550"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a>从 Configuration service 的全局知识库下载 ER 配置

[!include [banner](../includes/banner.md)]

本主题说明如何从 Configuration service 的全局知识库下载[电子申报 (ER) 配置](general-electronic-reporting.md#Configuration)。 有关详细信息，请参阅 [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services、Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration)。

## <a name="open-configurations-repository"></a>打开配置库

1. 使用以下角色之一登录到 Dynamics 365 Finance 应用程序：

    - 电子申报开发人员
    - 电子申报功能顾问
    - 系统管理员

2. 转到 **组织管理 > 工作区 > 电子申报**。
3. 在 **配置提供程序** 部分中，选择 **Microsoft** 磁贴。
3. 在 **Microsoft** 磁贴上，选择 **存储库**。

    ![电子申报工作区](./media/er-download-configurations-global-repo-er-workspace.png)

4. 在 **配置存储库** 页面，在网格中，选择 **全局** 类型的现有存储库。 如果此存储库没有显示在网格中，请执行以下步骤：

    1. 选择 **添加** 添加新存储库。
    2. 存储库类型选择 **全局**，然后选择 **创建存储库**。
    3. 如果系统提示，请按照授权说明操作。
    4. 为存储库输入名称和描述，然后选择 **确定** 确认新的存储库条目。
    5. 在网格中，选择 **全局** 类型的新存储库。

5. 选择 **打开** 查看选择的存储库的 ER 配置列表。

    ![配置存储库页面](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a>导入单个配置

1. 在 **配置存储库** 页面上的配置树中，选择所需的 ER 配置。
2. 在 **版本** 快速选项卡上，选择所选 ER 配置所需的版本。
3. 选择 **导入** 将所选版本从全局知识库下载到当前 Finance 实例。

    > [!NOTE]
    > **导入** 按钮对当前 Finance 实例中已呈现的 ER 配置版本不可用。

    ![配置存储库页面](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a>导入筛选的配置

1. 在 **配置存储库** 页面的配置树中，展开 **筛选器** 快速选项卡。
2. 在 **标记** 网格中，添加所需的任何标记。
3. 在 **国家/地区适用性** 字段中，选择适当的国家/地区代码，然后选择 **应用筛选器**。

    > [!NOTE]
    > **配置** 快速选项卡显示满足指定选择条件的所有配置。

4. 在 **配置** 快速选项卡上，选择 **导入** 将筛选出的配置从全局知识库下载到当前实例。
5. 在 **配置** 快速选项卡上，选择 **重置筛选器** 清理指定的选择条件。

    ![配置存储库页面](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> 根据 ER 设置，配置在导入后进行验证。 您可能会收到发现的任何不一致问题。 必须先解决这些问题，然后才可以使用导入的配置版本。 有关详细信息，请参阅本主题的相关资源列表。

> [!NOTE]
> ER 配置可以配置为依赖于其他配置。 因此，连同所选配置一起，其他配置可能会自动导入。 有关配置依赖关系的详细信息，请参阅[定义 ER 配置与其他组件之间的依赖关系](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)。

## <a name="additional-resources"></a>其他资源

[电子报告 (ER) 概览](general-electronic-reporting.md)
