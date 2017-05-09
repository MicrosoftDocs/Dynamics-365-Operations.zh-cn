---
title: "从 Lifecycle Services 下载电子申报配置"
description: "本主题介绍如何从 Microsoft Dynamics Lifecycle Services (LCS) 下载电子申报 (ER) 配置。"
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 9dca5dec846670da25926826f59d7bce0fa0dcea
ms.lasthandoff: 03/31/2017


---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>从 Lifecycle Services 下载电子申报配置

本主题介绍如何从 Microsoft Dynamics Lifecycle Services (LCS) 下载电子申报 (ER) 配置。

本教程指导您如何从 Microsoft Dynamics Lifecycle Services (LCS) 下载最新版本的电子申报 (ER) 配置的整个流程。

1.  通过使用以下角色之一登录到 Dynamics 365 for Operations：
    -   电子申报开发人员
    -   电子申报功能顾问
    -   系统管理员

2.  转到**组织管理** &gt; **电子申报**。
3.  在**配置提供程序**部分中，选择 **Microsoft** 磁贴。
4.  在 **Microsoft** 磁贴上，单击**存储库**。 [![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  在**配置存储库**页面，在网格中，选择 **LCS** 类型的现有存储库。 如果此存储库没有显示在网格中，请执行以下步骤：
    1.  单击**添加**添加新存储库。
    2.  选择 **LCS** 作为存储库类型。
    3.  单击**创建存储库**。
    4.  输入存储库的名称和描述。
    5.  单击**确定**确认新存储库条目。
    6.  在网格中，选择 **LCS** 类型的新存储库。

6.  单击**打开**查看选择的存储库的 ER 配置列表。 [![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  在左侧窗格的配置树中，选择您所需的 ER 配置。
8.  在**版本**快速选项卡上，选择所选 ER 配置所需的版本。
9.  单击“**导入**”将所选版本从 LCS 下载到当前 Dynamics 365 for Operations 实例。 **注意：**“**导入**”按钮对当前 Dynamics 365 for Operations 实例中已呈现的 ER 配置版本不可用。 [![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**注意：**根据 ER 设置，配置在导入后进行验证。 您可能会收到发现的任何不一致问题。 在可以使用导入的配置版本之前，必须解决这些问题。 有关详细信息，请参阅本主题的相关文章列表。

<a name="see-also"></a>请参阅
--------

[电子申报概览](general-electronic-reporting.md)


