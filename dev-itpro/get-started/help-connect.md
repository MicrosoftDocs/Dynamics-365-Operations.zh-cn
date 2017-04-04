---
title: "连接帮助系统"
description: "此主题介绍 Microsoft Dynamics 365 for Operations 帮助系统的组件，并且提供如何连接它们的概览以及如何创建自定义帮助的摘要。"
author: margoc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 5ac5e30cff2239f601778001368fa7aaba478f5c
ms.lasthandoff: 03/31/2017


---

# <a name="connect-the-help-system"></a>连接帮助系统

此主题描述以帮助系统的组件 Microsoft Dynamics 365 的操作。 它提供的概览如何连接这些组件和汇总如何创建自定义帮助。 

<a name="help-architecture"></a>帮助体系结构
-----------------

下图显示 Dynamics 365 部分的工序的帮助系统。 产品帮助系统都会从 Dynamics 365 的"层数的工序的 https://docs.microsoft.com 站点，以及任务在业务流程建模器在 Reporting Services Lifecycle Services (LCS) 引导存储。 
**注释：**含有星号 (\*) 的示意图列出的功能，计划，但不可用。 [![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>帮助系统的连接
**使用系统参数**页，系统管理员连接帮助系统的一部分部署的。 [![系统参数与设置] ("帮助。/media/system-parameters_ops-1024x437.png)](。**) /media/system-parameters_ops.png 在系统参数**页上，执行以下步骤：

1.  **重要：**该您首次打开帮助** **选项卡，则必须连接到 Lifecycle Services。 请确保{{在：in_the_middle_of}}中间窗体单击链接，等待连接，关闭对话框，然后单击**好**具有**系统参数**页。[! [] (LCS 到的连接。/media/connect 对 lcs 庄稼 1024x365.png“到”)] LCS 的连接 (。/media/connect 对 lcscrop.png)
2.  选择要连接到的 Lifecycle Services 项目。
3.  选择要从中检索任务录制的 BPM 库（在所选项目内）。
4.  选择 BPM 库的显示顺序。 它决定库中的任务录制在**“帮助”**窗格中的显示顺序。

在您完成这些步骤后，您可以打开**“帮助”**窗格并单击**“任务指南”**选项卡。 您现在将看到应用于您当前在 Dynamics 365 for Operations 中所处页面的任务指南。 如果未找到任何任务指南，您可以输入关键字来调整搜索。

### <a name="showing-translated-task-guides"></a>显示翻译的任务指南

转换的任务指南在 5 月 2016 APQC 统一的库和入门库中首先已装运。 在 Dynamics 365 for Operations 中，若要查看本地化的任务指南帮助，请确保您已连接到五月库。 任务指南的语言将为各个用户进行控制的设置。**按语言选项** &gt; **下**首选项。 **注意︰**虽然许多任务指南已被翻译了，但现在，Dynamics 365 for Operations 客户端不显示翻译的任务指南名称。 此外，在 2 月 2016 只下达的任务指南可用于转换"五月"库中。 我们将发布包含其它翻译的更新库。

-   如果已翻译任务指南，在您打开任务指南时，所有任务指南文本都将显示为您选择的语言。
-   如果尚未翻译任务指南，在您打开任务指南时，仅部分文本（控制文本）显示为您选择的语言。

## <a name="creating-custom-help"></a>创建客户帮助
您可以通过创建反映您的实施的任务录制并将其保存到 LCS 业务流程库中，为 Dynamics 365 for Operations 实施创建自定义帮助。 对于合作伙伴，如果您要将一个库提升到公司库并将其包括到解决方案中，它将可供您的客户使用。 您还可以复制 APQC Unified 全局库，然后打开您的副本，从它打开任务录制，然后修改它们，并保存具有所做更改的录制。 有关详细信息，请参阅创建培训的 [如何记录任务用作] (文档或。/user-interface/task-recorder.md)。

<a name="see-also"></a>请参阅
--------

[Help overview](help-overview.md)

[] (概览任务录制器。/user-interface/task-recorder.md)

[如何创建任务录制以用作文档或培训](../user-interface/task-recorder-training-docs.md)

[创建 Dynamics 365 的新库的培训的工序。Lifecycle Services 中使用任务录制器 (外部)] 链接 (https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)


