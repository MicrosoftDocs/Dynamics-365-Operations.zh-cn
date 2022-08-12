---
title: 导入更新后的 ER 配置版本
description: 本文说明如何从配置服务的全局存储库导入更新后的电子报告 (ER) 配置版本。
author: NickSelin
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0dac106a592a6a70aae6b245bce74d21c98cad10
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108430"
---
# <a name="import-updated-versions-of-er-configurations"></a>导入更新后的 ER 配置版本

[!include [banner](../includes/banner.md)]

电子申报 (ER) [存储库](general-electronic-reporting.md#Repository)用于共享 [ER 配置](general-electronic-reporting.md#Configuration)。 可以将不同存储库中的 ER 配置[导入](download-electronic-reporting-configuration-lcs.md)到您的 Microsoft Dynamics 365 Finance 实例中。 导入 ER 配置时，[配置提供程序](general-electronic-reporting.md#Provider)可以发布新[版本](general-electronic-reporting.md#component-versioning)存储库，以使其可共享。

本文说明如何从配置服务的全局存储库导入更新后的 ER 配置版本。 有关详细信息，请参阅 [Microsoft Dynamics 365 Finance - Regulatory Services、Configuration service](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration)。

## <a name="review-the-available-updated-versions"></a>检查可用的更新后版本

1. 通过使用以下角色之一登录到 Finance：

    - 电子申报开发人员
    - 电子申报功能顾问
    - 系统管理员

2. 转到 **组织管理** \> **工作区** \> **电子申报**。
3. 在 **本地化配置** 页面的 **相关链接** 部分中，选择 **导入配置版本更新**。

    ![本地化配置页面。](./media/er-download-updated-versions-global-repo1.png)

4. 在 **导入电子申报配置版本更新** 对话框的 **运行模式** 字段中，选择 **仅显示可用更新**。 然后选择 **确定**。 

    ![“运行模式”字段设置为“仅显示可用更新”。](./media/er-download-updated-versions-global-repo2.png)

5. 查看收到的消息。 这些消息提供有关当前 Finance 实例中的 ER 配置和有关其与全球存储库内容的比较的以下信息：

    - ER 配置总数
    - 全球存储库中不存在的 ER 配置
    - 当前 Finance 实例中已有其最新版本的 ER 配置（若要查看这些 ER 配置的完整列表，请选择 **消息详细信息** 链接。）

        ![“已导入了以下配置的最新版本”消息和消息详细信息](./media/er-download-updated-versions-global-repo3.png)

    - 全球存储库中有其最新版本且可导入到当前 Finance 实例的 ER 配置（若要查看这些 ER 配置的完整列表，请选择 **消息详细信息** 链接。）

        ![“可用更新”消息和消息详细信息](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a>导入可用的更新后版本

1. 通过使用以下角色之一登录到 Finance：

    - 电子申报开发人员
    - 电子申报功能顾问
    - 系统管理员

2. 转到 **组织管理** \> **工作区** \> **电子申报**。
3. 在 **本地化配置** 页面的 **相关链接** 部分中，选择 **导入配置版本更新**。
4. 在 **导入电子申报配置版本更新** 对话框的 **运行模式** 字段中，选择 **导入最新更新** 将最新的 ER 配置版本从全球存储库导入到当前 Finance 实例中。
5. 若要为导入计划批处理作业，请在 **在后台运行** 快速选项卡上，将 **批处理** 选项设置为 **是**。 如果要定期重复导入，请配置所需重复周期。

    ![“运行模式”字段设置为“导入最新更新”。](./media/er-download-updated-versions-global-repo5.png)

6. 选择 **确定**。
7. 若要了解已导入了哪些配置版本，请执行以下操作之一：

    - 如果以交互方式运行导入，而不是使用批处理作业运行导入，请查看收到的消息。

        ![以交互方式运行导入期间收到的消息。](./media/er-download-updated-versions-global-repo6.png)

    - 如果以批处理方式运行导入，请执行以下步骤：

        1. 转到 **通用** \> **查询** \> **批处理作业** \> **我的批处理作业**。
        2. 找到并选择 **导入电子申报配置版本更新** 作业，然后在操作窗格的 **批处理作业** 选项卡上，选择 **批处理作业历史记录** 查看作业历史记录。
        3. 在 **批处理作业历史** 页面上，选择 **日志**。 然后，在收到的消息中，选择 **消息详细信息** 链接查看作业日志。

        ![作业日志。](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> 建议不要计划定期批处理作业来将更新后的 ER 配置版本直接从全球存储库导入到生产环境中，因为导入的版本将立即可用。 而是改用这种方法将 ER 配置版本部署到沙盒环境。 然后可以先在沙盒环境中评估它们，之后才将其部署到生产环境。

## <a name="additional-resources"></a>其他资源

- [电子报告 (ER) 概览](general-electronic-reporting.md)
- [从 Configuration service 的全局知识库下载 ER 配置](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
