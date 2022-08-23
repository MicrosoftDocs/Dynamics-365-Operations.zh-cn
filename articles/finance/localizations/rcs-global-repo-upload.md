---
title: 在 RCS 中创建 ER 配置并上传到全局知识库
description: 本文介绍如何在 Microsoft Regulatory Configuration Services (RCS) 中创建电子报告 (ER) 配置并上传到全局知识库。
author: kfend
ms.date: 01/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
ms.openlocfilehash: 21e6ab3a7066fda23f1f5672f6f74bc6bd1ff1f6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282984"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>在 Regulatory Configuration Service (RCS) 中创建 ER 配置并上传到全局知识库

[!include [banner](../includes/banner.md)]

可使用 Microsoft Regulatory Configuration Services (RCS) 设计电子申报 (ER) 配置，然后发布，使其可在您的组织中使用。

以下过程介绍系统管理员或电子申报开发人员角色的用户如何创建已经在 RCS 实例中配置的 ER 配置的派生版本，然后将派生配置上传到全局知识库。 

必须先满足以下先决条件，才能完成这些过程：

- 有权访问组织的 RCS 环境。
- 创建一个可用的配置提供程序并将其设为活动状态。 有关详细信息，请参阅[创建配置提供程序并将其标记为有效](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。

必须确保为组织预配 RCS 环境。 如果您没有为组织预配 RCS 实例，则可以使用以下步骤执行此操作：

1. 在财务和运营应用中，转到 **组织管理** \> **工作区** \> **电子报告**。
2. 在 **相关链接/外部链接** 中，选择 **Regulatory services – 配置**，然后按照说明进行 **注册** 以预配一个。

如果已经为组织预配了 RCS 环境，请使用页面 URL 访问该环境，然后选择 **注册** 选项。

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>在 RCS 中创建配置的派生版本

> [!NOTE]
> 如果这是您第一次使用 RCS，则您将没有任何可供从中派生的配置。 您需要从全局存储库导入配置。 有关详细信息，请参阅[从 Configuration service 的全局知识库下载 ER 配置](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)。

1. **登录** RCS，然后选择 **电子申报** 工作区。
2. 验证您是否有适用于组织并且设置为活动状态的可用配置提供程序（请参阅先决条件）。 
3. 选择 **申报配置**。
4. 选择新版本的派生来源配置。 可以使用上面的筛选器字段缩小搜索范围。
5. 选择 **创建配置** \> **从名称派生**。
6. 输入名称和说明，然后选择 **创建配置** 创建“草稿”状态的新派生版本。
7. 选择新派生的配置，并在需要时对配置格式进行其他更改。 
8. 完成更改后，您需要将配置的 **更改状态** 设置为 **已完成**，以便能够将其发布到存储库。 选择 **确定**。

![RCS 中的新配置版本。](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> 更改配置状态之后，可能会收到与相连应用程序有关的验证错误消息。 若要关闭验证，请在操作窗格上的 **配置** 选项卡中，选择 **用户参数**，然后将 **配置状态更改时跳过验证并重定基本值** 选项设置为 **是** 

## <a name="upload-a-configuration-to-the-global-repository"></a>将配置上传到全局知识库

若要与组织共享新配置或派生配置，可以通过执行以下步骤将其上传到全局存储库：

1. 选择配置的已完成版本，然后选择 **上传到知识库中**。
2. 选择 **全局 (Microsoft)** 选项，然后选择 **上传**。

    ![“上传到知识库”选项。](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. 在配置消息框中选择 **是**。 
4. 按照需要更新版本说明，然后选择 **确定**。 您还可以有选择性地将版本上传到已连接的应用程序或 GIT 存储库。  

配置状态将更新为 **已共享**，并将配置上传到全局存储库中。 还创建了您上传的配置的草稿版本，如果需要后续更改，则可以使用该版本。

在将配置上传到全局存储库后，您可以通过以下方式使用该配置：

- 将其导入到您的 Dynamics 365 实例中。 有关详细信息，请参阅 [(ER) 从 RCS 导入配置](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md)。
- 与第三方或外部组织共享；请参阅 [RCS 与外部组织共享电子申报 (ER) 配置](rcs-global-repo-share-configuration.md)

    ![全局存储库中的派生内部统计 Contoso 配置版本。](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>从全局存储库中删除配置
完成以下步骤，删除您的组织创建的配置。

1. 在 **电子报告** 工作区中，确认您的配置提供程序是 **活动** 的。 有关详细信息，请参阅[创建配置提供程序并将其标记为有效](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。
2. 在活动的配置提供程序上，选择 **存储库**。
3. 选择存储库类型 **全局**，然后选择 **打开**。
4. 在 **筛选器** 快速选项卡上，使用 **筛选器** 功能找到要删除的配置。
5. 在 **版本** 快速选项卡上，选择要删除的配置版本，然后选择 **删除**：

    ![从全局存储库中删除配置。](media/RCS_Delete_from_GlobalRepo.JPG)

6. 在配置消息框中选择 **是**。

    ![删除配置版本确认消息。](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
配置版本已删除，并显示确认消息。 

> [!NOTE]
> 配置只能由创建配置的配置提供程序删除。 如果配置已与另一个组织共享，在删除配置之前，需要取消共享配置。
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

