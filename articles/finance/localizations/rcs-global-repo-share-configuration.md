---
title: 与外部组织共享 RCS/全局知识库中的 ER 配置
description: 此主题介绍如何直接与外部组织共享 Microsoft Regulatory Configuration Services (RCS)/全局知识库中的电子申报 (ER) 配置。
author: JaneA07
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: e7ec24ddc532ee3b87108d076d5103538be903be
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218822"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a>直接与外部组织共享 Regulatory Configuration Services (RCS) 全局知识库中的电子申报 (ER) 配置

[!include [banner](../includes/banner.md)]

可使用 Microsoft Regulatory Configuration Services (RCS) 共享电子申报 (ER) 配置，然后将其发布到外部组织。

以下过程介绍 RCS 用户如何与外部组织共享已在 RCS 实例中配置的 ER 配置版本。 必须先满足以下先决条件，才能完成这些过程：

- 访问 RCS 实例。
- 创建有效配置提供程序。 有关详细信息，请参阅[创建配置提供程序并将其标记为有效](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。
- 新建并上传 ER 配置版本。 有关详细信息，请参阅[新建和上传电子申报 (ER) 配置版本](rcs-global-repo-upload.md)。

还必须确保为公司预配 RCS 环境。

1. 在 Finance and Operations 应用中，转到 **组织管理** \> **工作区** \> **电子申报**。
2. 如果没有为公司预配 RCS 环境，请选择 **Regulatory services – 配置外部**，然后按照说明预配一个。

如果已经为公司预配了 RCS 环境，请通过选择登录选项使用页面 URL 访问该环境。

## <a name="verify-the-configuration-that-you-want-to-share"></a>验证要共享的配置

执行以下步骤验证是否已将要共享的配置上传到了全局知识库。

1. 在 **电子申报** 工作区中，选择配置提供程序的 **知识库**。

    ![配置提供程序](media/1_RCS_Repo_for_config_provider.JPG)

2. 选择 **全局知识库**\>**打开**。
3. 搜索要共享的配置。 可以使用筛选器字段缩小搜索范围。 如果在全局知识库中找不到此配置，请执行[新建和上传电子申报 (ER) 配置版本](rcs-global-repo-upload.md)中的步骤。

## <a name="share-er-configurations-with-external-organizations"></a>与外部组织共享 ER 配置

在配置提供程序下创建了配置之后，可以通过使用 **全局配置知识库** 页中的 **共享对象** 快速选项卡直接与外部组织共享。

1. 在 **电子申报** 工作区中，选择配置提供程序的 **知识库**。
2. 选择 **全局知识库**\>**打开**。 
3. 选择要共享的配置。
4. 在 **共享对象** 快速选项卡上，选择 **组织**。

    ![“共享对象”快速选项卡](media/1_RCS_Repo_for_Share_with_org.JPG)

5. 在此对话框中，输入外部组织的域名，然后选择 **确定**。

    ![“与外部组织共享配置版本”对话框](media/1_RCS_Repo_for_Share_with_form.JPG)

将与外部组织共享配置，并在全局知识库中提供给该组织。 可以在这里将其导入到组织的 RCS 实例中或其 Finance and Operations 应用实例中。

6. 若要取消更新之前已经与外部组织共享的配置，请选择该配置，然后单击 **取消更新**，再选择 **确定**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]