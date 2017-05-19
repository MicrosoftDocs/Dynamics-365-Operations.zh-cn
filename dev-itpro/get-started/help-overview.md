---
title: "帮助概览"
description: "本文提供 Microsoft Dynamics 365 for Operations 帮助系统的组件的概览。 另外还说明如何向您的组织提供自定义文档和培训。"
author: margoc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16381
ms.assetid: 018c148c-9cbd-41e0-8186-d75dbf66288f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6f785ac8b9a8be503bf9122f21716f745b17115b
ms.openlocfilehash: f08434b4c818460009644e77da1b37ba86cc1d54
ms.contentlocale: zh-cn
ms.lasthandoff: 04/27/2017


---

# <a name="help-overview"></a>帮助概览

[!include[banner](../includes/banner.md)]


本文提供 Microsoft Dynamics 365 for Operations 帮助系统的组件的概览。 另外还说明如何向您的组织提供自定义文档和培训。 

Dynamics 365 for Operations 包括一个帮助系统，基于两个主要组件：

-   文档站点
-   任务指南

您可以从 Dynamics 365 for Operations 中的“帮助”窗格访问文章和任务指南，如下面的屏幕快照所示。 [![“帮助”窗格](./media/help-pane-ops-task-guides-1024x741.png)](./media/help-pane-ops-task-guides.png)本文描述帮助系统，并说明如何为您的组织创建自定义文档和培训资源。

## <a name="help-on-docsmicrosoftcom"></a>docs.microsoft.com 中的“帮助”
docs.microsoft.com 站点 ([docs.microsoft.com/dynamics365/operations](/dynamics365/#pivot=solutions&panel=solutions_operations) 是 Dynamics 365 for Operations 的产品文档的主要来源。 该站点提供以下功能：

-   **访问最新的内容** – 该站点能让我们以更快、更灵活的方式创建、交付和更新产品文档。 因此，它有助于确保您有权访问最新技术信息。
-   **由专家编写的内容** – 该站点提供更丰富的产品文档集，可由 Microsoft 内外的社区成员增强。
-   **访问不同类型的内容** – 该站点能让您快速访问有关 Dynamics 365 for Operations 的不同类型的内容，如 Microsoft Office 组合演示文稿、任务指南、视频和主题。
-   **支持您的业务流程的内容** – 该站点包括侧重于业务流程的内容，这些内容利用 Microsoft Dynamics Lifecycle Services (LCS) 中的 Business Process Modeler (BPM)。

我们已将以前的帮助 wiki 中的所有内容迁移到了 docs。 我们对新的站点感到非常激动，希望您也是。

### <a name="when-can-we-use-it"></a>我们什么时候可以使用它？

您可以立即阅读 docs 上的内容 -- 它是完全公共的、可搜索的，而无需登录。 您可以使用您喜爱的任何搜索引擎查找内容。 如果您愿意，可以通过登录评论该站点的文章。


## <a name="task-guides"></a>任务指南
任务指南是受控的、引导式、交互式的体验，带领您完成任务或业务流程中的步骤。 您可以从“帮助”窗格中打开（播放）任务指南。 当您首次单击任务指南时，“帮助”窗格将显示任务的分步说明。 本地化的任务指南现已提供。 [![任务指南阅读视图](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png) 若要开始引导式、交互式的体验，请在“帮助”窗格底部单击**启动任务指南**。 黑色指针打开并指示您必须执行的操作。 按照 UI 中显示的指导进行操作，并按照指示输入数据。 [![任务指南步骤说明](./media/task-guide-step-1-ops.png)](./media/task-guide-step-1-ops.png) **重要信息：**您在播放任务指南时输入的数据是真实的。 如果您处于生产环境中，则数据将输入您当前使用的公司中。

### <a name="it-all-begins-with-task-recorder"></a>它全都从任务录制器开始

任务是通过使用任务录制器创建的。 当您使用任务录制器时，您在 Dynamics 365 for Operations UI 中执行的所有操作（如单击菜单、更改设置和输入数据）都将被记录。 您记录的步骤统称为任务录制。 如同我们在前一部分说明的，任务录制可以显示在“帮助”窗格中和作为任务指南播放。 不过，您可以通过其他方法来使用任务录制：

-   **将任务录制保存到 BPM** – 可以将任务录制保存到 LCS 中的一个 BPM 库中的层次结构行。 当您将任务录制保存到 BPM 时，会连同录制的步骤一起，生成并显示流程图。 **注释：**若要在 Dynamics 365 for Operations 的“帮助”窗格中显示任务录制并将其作为任务指南播放，您必须将录制保存到 BPM 库。
-   **将任务录制保存为 Word 文档** – 通过将任务录制保存为 Microsoft Word 文档，您可以轻松地为您的组织生成可打印的培训指南。

有关任务录制器的详细信息，请参阅 [Dynamics 365 for Operations 中的任务录制器](../user-interface/task-recorder.md)。

### <a name="creating-customized-task-recordings"></a>创建自定义的任务录制

您可以创建自己的任务录制，也可以下载 Microsoft 提供的自定义任务录制。 因此，您可以为您的组织创建反映您的特定 Dynamics 365 for Operations 实施的自定义帮助。 若要在 Dynamics 365 for Operations 的“帮助”窗格中显示任务录制并将其作为任务指南播放，您必须将录制保存到 LCS 中的 BPM 库。 如果您是合作伙伴，并且您要将一个库提升到公司库并将其包括到解决方案中，它将可供您的客户使用。 有关完整指南，请参阅[使用任务录制创建文档或培训](../user-interface/task-recorder.md)。

## <a name="in-product-help"></a>产品内帮助
若要访问 Dynamics 365 for Operations 内的帮助内容，请单击**“帮助”**(**?**) 图标，然后选择“帮助”或按 Ctrl+Shift+?。 在这两种情况下，“帮助”窗格将会打开。 从“帮助”窗格中，您可以访问文章或任务指南。 [![帮助窗格](./media/help-pane-wiki-1024x684.png)](./media/help-pane-wiki.png)

### <a name="accessing-articles-from-the-help-pane"></a>从“帮助”窗格中访问文章

从“帮助”窗格中，您可以访问适用于 Dynamics 365 for Operations 客户端的文章。 在您首次打开“帮助”窗格并单击 **Wiki** 选项卡时，您将看到适用于您当前在 Dynamics 365 for Operations 中所处页面的文章。 如果未找到任何文章，您可以输入关键字来调整搜索。 当您在“帮助”窗格中单击一篇文章时，新的选项卡会在 Web 浏览器中打开并显示文章。 

### <a name="accessing-task-guides-from-the-help-pane"></a>从“帮助”窗格中访问任务指南

在您可以从“帮助”窗格中访问任务指南前，系统管理员必须转到 Dynamics 365 for Operations 中的**系统参数**页并配置某些设置。 **注意：**

-   为了配置帮助，您必须使用在其中部署 Dynamics 365 for Operations 的租户的帐户登录。
-   不能从在本地虚拟硬盘 (VHD) 中运行的 Dynamics 365 for Operations 的实例连接到 LCS 库。

[![具有帮助设置的系统参数窗体](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) 在**系统参数**页上，执行以下步骤：

1.  **重要：**首次打开"帮助"选项卡时，必须连接到 Lifecycle Services。 请确保单击窗体中间的链接，等待连接，关闭对话框，单后单击“确定”以转至参数窗体。[![连接至 LCS](./media/connect-to-lcs-crop-1024x365.png)](./media/connect-to-lcs-crop.png)
2.  选择要连接到的 Lifecycle Services 项目。
3.  选择要从中检索任务录制的 BPM 库（在所选项目内）。
4.  选择 BPM 库的显示顺序。 它决定库中的任务录制在“帮助”窗格中的显示顺序。

在系统管理员完成这些步骤后，您可以打开“帮助”窗格并单击**任务指南**选项卡。 您现在将看到应用于您当前在 Dynamics 365 for Operations 中所处页面的任务指南。 如果未找到任何任务指南，您可以输入关键字来调整搜索。 您在“帮助”窗格中单击一个任务指南后，“帮助”窗格会显示分步说明，而且您可以播放该任务指南。 [![任务指南阅读视图](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png)

### <a name="where-are-the-translated-task-guides"></a>翻译的任务指南在哪里？

翻译后的任务指南在标题中带有“所有语言”的库中发布。 在 Dynamics 365 for Operations 中，若要查看本地化的任务指南帮助，请确保您已连接到相应库。 每个用户的任务指南的显示语言由**选项** &gt; **首选项**下的“语言设置”控制。 
-   如果已翻译任务指南，在您打开任务指南时，所有任务指南文本都将显示为您选择的语言。
-   如果尚未翻译任务指南，在您打开任务指南时，仅部分文本（控制文本）显示为您选择的语言。

## <a name="additional-resources"></a>其他资源
下表列出提供 Dynamics 365 for Operations 内容的网站。 我们的内容网站经过了组织，用以支持客户生命周期。 每个阶段由不同站点集支持。 名称旁边具有星号 (\*) 的站点要求您使用与服务计划关联的帐户登录。

| 站点                                                                     | 说明                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Docs.microsoft.com](/dynamics365/#pivot=solutions&panel=solutions_operations) | 承载或链接到 Dynamics 365 for Operations 的所有产品文档。                                                                                                                                                               |
| [Lifecycle Services](http://lcs.dynamics.com/en/)\*                      | 提供基于云的协作工作区，可供客户和合作伙伴用来从售前到执行和运营阶段管理 Dynamics 365 for Operations 项目。 此站点在执行的所有阶段都很有用。 |
| [CustomerSource](http://www.customersource.com/)\*                       | 承载广泛的培训资源，并且是 Dynamics 365 for Operations 的主要支持站点。 可能需要登录才能访问该站点上的特定资源。                                                                      |
| [支持博客](http://aka.ms/AXSupportBlog)                              | 提供 Dynamics 365 for Operations 支持团队发布的提示和窍门。                                                                                                                                                  |
| [MSDN](http://aka.ms/AXMSDN)                                             | 承载为开发人员编写的来自以前版本的内容。                                                                                                                                                                       |
| [TechNet](http://aka.ms/TechNet)                                         | 承载 IT 专业和应用程序用户编写的来自以前版本的内容。                                                                                                                                           |
| [Dynamics 社区](http://community.dynamics.com/)                  | 承载博客、论坛和视频。                                                                                                                                                                                                           |
| [Microsoft.com/Dynamics/](http://www.microsoft.com/dynamics/)                 | 提供评估和销售信息。                                                                                                                                                                                                 |



<a name="see-also"></a>请参阅
--------

[Dynamics 365 for Operations 帮助系统（可下载资料页）](https://mbs.microsoft.com/files/public/CS/AX2012R3/DynamicsAXHelpSystemFactSheet.pdf)

[Microsoft Dynamics 365 for Operations 中的任务录制器](../user-interface/task-recorder.md)

[使用任务录制创建文档或培训](../user-interface/task-recorder.md)

[新的或更新任务指南（2016 年 11 月）](new-task-guides-november-2016.md)
[新的或更新任务指南（2016 年 8 月）](new-updated-task-guides-available-august-2016.md)
[新的或更新任务指南（2016 年 5 月）](new-updated-task-guides-available-may-2016.md)
[新的或更新任务指南（2016 年 2 月）](new-task-guides-available-february-2016.md)








