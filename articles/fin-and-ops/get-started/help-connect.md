---
title: 连接帮助系统
description: 此主题介绍 Microsoft Dynamics 365 for Finance and Operations的“帮助”系统的组件，并且提供如何连接它们的概览以及如何创建自定义帮助的摘要。
author: margoc
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 929e453987c6e2773d1886d03a4393a68033566b
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850893"
---
# <a name="connect-the-help-system"></a>连接帮助系统

[!include [banner](../includes/banner.md)]

此主题介绍了 Microsoft Dynamics 365 for Finance and Operations 的帮助系统的组件。 它提供如何连接这些组件的概览和如何创建自定义帮助的摘要。

## <a name="help-architecture"></a>帮助体系结构

下图显示 Finance and Operations 帮助系统的各个部分。 产品内帮助系统从 Finance and Operations 站点 https://docs.microsoft.com 拉取文章，以及 Lifecycle Services (LCS) 中的业务流程建模器中存储的任务指南。

> [!NOTE]
> 图形中列出的带有星号 (\*) 的功能已计划，但还不可用。

[![帮助体系结构](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>连接帮助系统

> [!NOTE]
> **任务指南**选项卡目前在 Microsoft Dynamics 365 for Talent 和 Microsoft Dynamics 365 for Retail 中不可用。 我们目前正在努力在将来的版本中启用此功能。 Talent 中的入门中的任务指南体验可用，以涵盖基本功能。 docs.microsoft.com 站点 ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) 上还提供用于 Retail 和 Talent 的过程帮助。

使用**系统参数**页，系统管理员连接有关实施的部分帮助系统。

[![具有帮助设置的系统参数窗体](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

在**系统参数**页上，执行以下步骤：

> [!IMPORTANT]
> 首次打开**帮助**选项卡时，必须连接到 Lifecycle Services。 请确保单击窗体中间的链接，等待连接，关闭对话框，单后单击**确定**以转至**系统参数**页面。
>
> [![连接到 LCS](./media/connect-to-lcs-crop-1024x365.png "连接到 LCS")](./media/connect-to-lcs-crop.png)

1. 选择要连接到的 Lifecycle Services 项目。
2. 选择要从中检索任务录制的 BPM 库（在所选项目内）。

    - 对于 Finance and Operations 的 Microsoft 内容，选择 Finance and Operations 最新的 APQC 标准库。
    - 对于 Retail，我们将在不久后发布一个库。
    - 您无需为 Talent 选择库，因为已经为您建立了与正确库的连接。

3. 选择 BPM 库的显示顺序。 它决定库中的任务录制在**帮助**窗格中的显示顺序。

完成这些步骤后，您可以打开**帮助**窗格并单击**任务指南**选项卡。您现在将看到适用于您当前在 Finance and Operations 中所处页面的任务指南。 如果未找到任何任务指南，您可以输入关键字来调整搜索。

### <a name="showing-translated-task-guides"></a>显示翻译的任务指南

翻译的任务指南首次随 2016 年 5 月 APQC 标准库和入门库提供。 在 Finance and Operations 中，若要查看本地化的任务指南帮助，请确保您已连接到五月库。 每个用户的任务指南的显示语言由**选项** &gt; **首选项**下的语言”设置控制。

> [!NOTE]
> 虽然许多任务指南已被翻译了，但现在，Finance and Operations 客户端不显示翻译的任务指南名称。 此外，五月库中仅提供在 2016 年 2 月发布的任务指南的翻译。 我们将发布包含其它翻译的更新库。
>
> - 如果已翻译任务指南，在您打开任务指南时，所有任务指南文本都将显示为您选择的语言。
> - 如果尚未翻译任务指南，在您打开任务指南时，仅部分文本（控制文本）显示为您选择的语言。

## <a name="creating-custom-help"></a>创建客户帮助

您可以使用任务指南创建自定义帮助，或者将网站连接到帮助窗格。

### <a name="create-custom-help-with-task-guides"></a>使用任务指南创建定制帮助

您可以通过创建反映您的实施的任务录制并将其保存到 LCS 业务流程库中，为 Finance and Operations 和 Retail 创建自定义帮助。 您无法为 Talent 创建自定义任务指南。

对于合作伙伴，如果您要将一个库提升到公司库并将其包括到解决方案中，它将可供您的客户使用。 您还可以复制 APQC Unified 全局库，然后打开您的副本，从它打开任务录制，然后修改它们，并保存具有所做更改的录制。 有关详细信息，请参阅[如何创建任务录制以用作文档或培训](../../dev-itpro/user-interface/task-recorder.md)。

### <a name="connect-a-custom-site"></a>连接自定义站点

Microsoft 提供了介绍如何创建自定义帮助站点并将其连接到帮助窗格的白皮书和示例代码。 有关详细信息，请参阅：

- [为 Finance and Operations 创建自定义帮助（白皮书）](https://go.microsoft.com/fwlink/?linkid=2041185)
- [自定义帮助 GitHub 知识库](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a>其他资源

[帮助概览](help-overview.md)

[任务录制器概览](../../dev-itpro/user-interface/task-recorder.md)

[如何创建任务录制以用作文档或培训](../../dev-itpro/user-interface/task-recorder-training-docs.md)
