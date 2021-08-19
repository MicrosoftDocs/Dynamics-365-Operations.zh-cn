---
title: 在 RCS 中创建 ER 配置并上传到全局知识库
description: 此主题介绍如何在 Microsoft Regulatory Configuration Services (RCS) 中创建电子申报 (ER) 配置并上传到全局知识库。
author: JaneA07
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: b8be53c415d3b0c0fd057bb0d9c51b391d1c0c7471610c861909344059803441
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727213"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>在 Regulatory Configuration Service (RCS) 中创建 ER 配置并上传到全局知识库

[!include [banner](../includes/banner.md)]

可使用 Microsoft Regulatory Configuration Services (RCS) 设计电子申报 (ER) 配置，然后发布，使其可在您的组织中使用。

以下过程介绍系统管理员或电子申报开发人员角色的用户如何创建已经在 RCS 实例中配置的 ER 配置的派生版本，然后将派生配置上传到全局知识库。 

必须先满足以下先决条件，才能完成这些过程：

- 访问 RCS 实例。
- 创建有效配置提供程序。 有关详细信息，请参阅[创建配置提供程序并将其标记为有效](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。

还必须确保为公司预配 RCS 环境。

1. 在 Finance and Operations 应用中，转到 **组织管理** \> **工作区** \> **电子申报**。
2. 如果没有为公司预配 RCS 环境，请选择 **Regulatory services – 配置外部**，然后按照说明预配一个。

如果已经为公司预配了 RCS 环境，请通过选择登录选项使用页面 URL 访问该环境。

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>在 RCS 中创建配置的派生版本

1. 在 **电子申报** 工作区中，验证您是否有组织的有效配置提供程序。 
2. 选择 **申报配置**。
3. 选择新版本的派生来源配置。 可以使用上面的筛选器字段缩小搜索范围。
4. 选择 **创建配置** \> **从名称派生**。
5. 输入名称和说明，然后选择 **创建配置** 创建新的派生版本。
6. 选择新派生的配置，添加版本说明，然后选择 **确定**。 配置的状态将更改为 **已完成**。

![RCS 中的新配置版本。](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> 更改配置状态之后，可能会收到与相连应用程序有关的验证错误消息。 若要关闭验证，请在操作窗格上的 **配置** 选项卡中，选择 **用户参数**，然后将 **配置状态更改时跳过验证并重定基本值** 选项设置为 **是** 

## <a name="upload-a-configuration-to-the-global-repository"></a>将配置上传到全局知识库

若要与组织共享新配置或派生配置，可以将其上传到全局知识库。

1. 选择配置的已完成版本，然后选择 **上传到知识库中**。
2. 选择 **全局 (Microsoft)** 选项，然后选择 **上传**。

    ![“上传到知识库”选项。](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. 在配置消息框中选择 **是**。 
4. 按照需要更新版本说明，然后选择 **确定**。 

配置状态将更新为 **共享**，并将配置上传到全局知识库中。 可以在此处按照下面的方法进行处理：

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