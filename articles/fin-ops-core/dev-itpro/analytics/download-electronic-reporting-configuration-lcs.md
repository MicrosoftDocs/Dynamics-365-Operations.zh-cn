---
title: 从 Lifecycle Services 下载电子报告配置
description: 本文介绍如何从 Microsoft Dynamics Lifecycle Services (LCS) 下载电子申报 (ER) 配置。
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8ba720f997981e85ea08d532f23341a838533ac4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885285"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>从 Lifecycle Services 下载电子报告配置

[!include [banner](../includes/banner.md)]

本文介绍如何从 Microsoft Dynamics Lifecycle Services (LCS) 中的[共享资产库](../lifecycle-services/asset-library.md)下载最新版本的[电子申报 (ER) 配置](general-electronic-reporting.md#Configuration)。

> [!IMPORTANT]
> 使用 LCS 作为 ER 配置的存储库将[弃用](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release)。 有关详细信息，请参阅 [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) 存储弃用](../../../finance/localizations/rcs-lcs-repo-dep-faq.md)。

1. 通过使用以下角色之一登录到应用程序：

    - 电子申报开发人员
    - 电子申报功能顾问
    - 系统管理员

2. 转到 **组织管理** &gt; **工作区** &gt; **电子申报**。
3. 在 **配置提供程序** 部分中，选择 **Microsoft** 磁贴。
4. 在 **Microsoft** 磁贴上，选择 **存储库**。

    [![本地化配置页面上的 Microsoft 磁贴。](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. 在 **配置存储库** 页面，在网格中，选择 **LCS** 类型的现有存储库。 如果此存储库没有显示在网格中，请执行以下步骤：

    1. 选择 **添加** 添加存储库。
    2. 选择 **LCS** 作为存储库类型。
    3. 选择 **创建存储库**。
    4. 如果系统提示您提供授权信息，请按照屏幕上的说明操作。
    5. 输入存储库的名称和描述。
    6. 选择 **确定** 确认新存储库条目。
    7. 在网格中，选择 **LCS** 类型的新存储库。

6. 选择 **打开** 查看选择的存储库的 ER 配置列表。

    [![配置存储库页面。](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

    > [!TIP]
    > 如果访问 LCS 存储库以从 LCS 中的共享资产库下载配置时遇到问题，可以改为从[全局存储库](er-download-configurations-global-repo.md)下载配置。

7. 在左侧窗格的配置树中，选择所需 ER 配置。
8. 在 **版本** 快速选项卡上，选择所选 ER 配置所需的版本。
9. 选择 **导入** 将所选版本从 LCS 下载到当前实例。

    > [!NOTE]
    > **导入** 按钮对当前实例中已呈现的 ER 配置版本不可用。

    [![配置存储库页面。](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> 根据 ER 设置，配置在导入后进行验证。 您可能会收到发现的任何不一致问题。 在可以使用导入的配置版本之前，必须解决这些问题。 有关详细信息，请参阅本文的相关主题列表。

## <a name="additional-resources"></a>其他资源

[电子报告 (ER) 概览](general-electronic-reporting.md)

[从 Configuration service 的全局知识库下载 ER 配置](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
