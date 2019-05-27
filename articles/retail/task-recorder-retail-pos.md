---
title: Retail Modern POS (MPOS) 和 Cloud POS 的任务录制器和帮助
description: 此主题介绍如何在 Retail Modern POS 和 Cloud POS 中使用任务录制器。
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a74a1275f08e3dba60a1002a102e143eb37fcd9a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548546"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a>Retail Modern POS (MPOS) 和 Cloud POS 的任务录制器和帮助

[!include [banner](includes/banner.md)]

此主题介绍如何在 Retail Modern POS 和 Cloud POS 中使用任务录制器。

## <a name="overview"></a>概览

Retail Modern POS 或 Cloud POS 中的任务录制器是一个新解决方案，注重高响应性。 它提供灵活的应用程序编程接口 (API) 以实现可扩展性，并提供与业务流程录制的使用者的无缝集成。 此外，还提供了任务录制器与 Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) 上的业务流程建模器 (BPM) 工具的集成。 因此，用户能够继续从录制生成丰富的业务流程图来分析和设计自己的应用程序。

## <a name="architecture"></a>体系结构

任务录制器可以在客户端非常精确地录制用户操作。 每一项控制都会被全面感知，以通知任务录制器用户操作的执行。 控制通知任务录制器发生的事件，并实时传递相应用户操作的所有相关信息。 通过此信息，任务录制器可以捕获用户是操作的类型（如按钮单击、值输入或导航），以及所有与用户操作相关的数据（如输入数据值和类型、表单上下文或记录上下文）。 任务录制器继续显示包含足够详细信息的信息，以帮助保证录制播放可以准确地执行录制的操作，就如同用户在执行。 （Retail modern POS 或 Cloud POS 尚未实现播放功能。）

## <a name="basic-configuration"></a>基本配置

要在 POS 启用任务录制，请执行以下步骤。

1. 单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **收银机**。
2. 单击收银机启用任务录制。
3. 在**收银机**选项卡，在**常规**快速选项卡，将**启用任务录制**选项设置为**是**。
4. 单击**保存**。
5. 转到**零售** &gt; **零售 IT** &gt; **配送计划**。
6. 选择**收银机 (1090)** 作业，然后单击**立即运行**。

## <a name="create-a-recording"></a>创建录制

执行以下步骤使用任务录制器创建新录制。

1. 启动 Retail Modern POS 或 Cloud POS，并登录。
2. 在**设置**页，在**任务录制器**部分，单击**打开任务录制器**。 **任务录制器**窗格出现。 在开始新录制前，您可以单击右上角的**关闭**按钮 (**X**) 关闭**任务录制器**窗格。 若要重新打开窗格，请重复执行步骤 2。

    [![任务录制器窗格](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)

3. 输入录制的名称和描述，然后单击**开始**。 单击**开始**后，录制会话随即开始。

    > [!NOTE]
    > 如果您在录制正在进行时单击右上角的**关闭**按钮 (**X**)，**任务录制器**窗格将关闭，但录制会话不会结束。 若要重新打开任务录制器窗格，单击屏幕顶部的**帮助**按钮（问号）。
    >
    > [![问号](./media/help.jpg)](./media/help.jpg)

4. 单击**开始**后，任务录制器进入录制模式。 **任务录制器**窗格显示与录制流程相关的信息和控制。
5. 执行您希望在 Retail Modern POS 或 Cloud POS 用户界面 (UI) 执行的操作。
6. 若要结束录制会话，单击**停止**。

## <a name="download-options"></a>下载选项

在结束录制会话后，多个选项将显示，以便您可以下载您的录制。

[![下载选项](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)

### <a name="save-to-this-pc"></a>保存到此 PC

您可以使用录制包播放任务指南、维护录制或者编辑录制中的注释。 （Retail Modern POS 和 Cloud POS 尚未实现此功能。）

### <a name="export-as-word-document"></a>导出为 Word 文档

您可以将录制作为 Microsoft Word 文档保存。 此文档将包含录制的步骤和捕获的屏幕快照。

### <a name="save-as-developer-recording"></a>另存为开发人员录制

原始录制文件对于开发人员方案（如测试代码生成）很有用。 （此功能尚未实现。）

## <a name="recording-controls"></a>录制控制

[![录制控制](./media/controls.jpg)](./media/controls.jpg)

### <a name="stop"></a>停止

单击**停止**可结束录制会话。 请注意，会话在结束后不能重新启动。 因此，在结束之前请确保录制已完成。

### <a name="pause"></a>暂停

单击**暂停**可临时停止（暂停）录制会话并继续执行操作。 在单击**暂停**后执行的步骤不会被录制。

### <a name="continue"></a>继续

要恢复录制会话，在暂停后单击**继续**。

### <a name="capture-screenshots"></a>捕获屏幕快照

任务录制器可以在您录制业务流程时捕获 Retail Modern POS UI 的屏幕快照。 若要开启屏幕快照捕获功能，将**捕捉屏幕快照**选项设置为**是**，然后进行录制。 录制完成后，单击**停止**并下载 Word 文档。 文档将包含具有相关屏幕截图的步骤。

> [!NOTE]
> Cloud POS 不支持捕获屏幕快照功能。

### <a name="start-task-and-end-task"></a>开始任务和结束任务

可以通过使用**开始任务**和**结束** **任务**按钮来指定一组已分组步骤的开始和结束。 单击**开始任务**添加“开始任务”步骤，然后执行组中应包括的步骤。 在您完成该组步骤的执行后，单击**结束任务**。 任务帮助您组织您的过程。 任务可以嵌套在其他任务内。 这样，您就可以更好地组织非常长的复杂业务流程。

## <a name="adding-annotations"></a>添加注释

注释是您在录制中添加到步骤的其他文本。 例如，您可以使用注释为用户提供更多上下文或说明。 您可以在一个步骤之前或之后添加注释。 您可以通过单击步骤右侧的**编辑**按钮（铅笔符号）将注释添加到任何步骤。

[![编辑步骤的按钮](./media/annotate.jpg)](./media/annotate.jpg)

### <a name="texts-and-notes"></a>文本和注释

您可以使用**文本**和**注释**字段来添加应与任务指南中的步骤关联的文本。

[![文本和注释字段](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)

#### <a name="text"></a>文本

在**文本**字段中输入的文本将在任务指南的步骤文本*上方*显示。 此位置适合您希望用户在完成步骤前阅读的文本。

#### <a name="notes"></a>注释

在**注释**字段中输入的文本将在任务指南的步骤文本*下方*显示。 若要阅读注释文本，用户必须在弹出窗口中展开步骤文本。 此位置适合可能对用户有用，但用户完成操作所不需要的可选阅读材料或其他信息。

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a>Retail Modern POS 和 Cloud POS 中的帮助

要在 Retail Modern POS 和 Cloud POS 的“帮助”窗格中显示您自己的自定义任务录制以便它们可作为文本查看，您必须将任务录制保存到自己的 BPM 库，然后更新帮助系统参数以指向您的 BPM 库。 有关更多信息，请参阅 [连接帮助系统](../fin-and-ops/get-started/help-connect.md)。 Retail Modern POS 和 Cloud POS 帮助实时搜索 LCS。 它搜索在 Microsoft Dynamics 365 for Retail 帮助系统参数中选择的所有 BPM 库，并显示相关结果。 若要访问**帮助**菜单，单击屏幕顶部的**帮助**按钮（问号），然后在搜索框中键入流程名称并点击搜索按钮。

[![帮助按钮](./media/help.jpg)](./media/help.jpg)

当您在搜索结果中单击任务指南时，可以作为帮助主题查看步骤或将步骤导出到 Word 文档。

> [!NOTE]
> Retail Modern POS 和 Cloud POS 中的帮助不会根据您所处的窗体或正在执行的操作提供任务指南。 您必须输入在搜索框中键入流程名称，然后单击**搜索**。
