---
title: 创建工作流概览
description: 本主题介绍如何创建工作流。
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: 23fe13f7e3c7e8138b690c96fafc075c4700a60f
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693298"
---
# <a name="create-workflows-overview"></a>创建工作流概览

[!include [banner](../includes/banner.md)]

本主题介绍如何创建工作流。

## <a name="open-the-workflow-editor"></a>打开工作流编辑器

您正在使用的模块将确定可以创建的工作流的类型。 按照以下步骤选择工作流的类型，以创建并打开工作流编辑器。

1. 打开要为其创建新工作流的模块。 例如，要为采购申请创建工作流，单击 **采购**。
2. 单击 **设置**&gt;**\[模块名称\]工作流**。
3. 在显示的列表页上的“操作窗格”上，单击 **新建**。
4. 在 **创建工作流** 页面上，选择要创建的工作流类型，然后单击 **创建工作流**。 将显示工作流编辑器。 您现在可以使用以下过程来设计工作流。

## <a name="drag-workflow-elements-onto-the-canvas"></a>将工作流元素拖到画布上

工作流编辑器的 **工作流元素** 区域包含您可以添加到工作流的元素。 要在工作流中添加元素，将元素拖到画布上。

## <a name="connect-the-elements"></a>连接元素

要将一个工作流元素连接到另一个元素，则将指针悬停在该元素上方，直到连接点显示。 单击连接点并将其复制到另一个元素。 确保连接所有元素。

## <a name="configure-the-properties-of-the-workflow"></a>配置工作流的属性

按照以下步骤配置工作流的属性。

1. 单击画布，确保未选择任何工作流元素。
2. 单击 **属性** 以打开工作流的 **属性** 页面。
3. 按照[配置工作流属性](configure-workflow-properties.md)主题中的步骤进行操作。

## <a name="configure-the-elements-of-the-workflow"></a>配置工作流元素

配置您拖到画布中的各个元素。 有关如何配置各个工作流元素的信息，请参阅以下主题：

- [配置工作流中的手动任务](configure-manual-task-workflow.md)
- [配置工作流中的自动化任务](configure-automated-task-workflow.md)
- [配置工作流中的审核流程](configure-approval-process-workflow.md)
- [配置工作流中的审核步骤](configure-approval-step-workflow.md)
- [配置工作流中的手动决策](configure-manual-decision-workflow.md)
- [配置工作流中的有条件决策](configure-conditional-decision-workflow.md)
- [配置工作流中的并行分支](configure-parallel-activity-workflow.md)
- [配置并行分支](configure-parallel-branch-workflow.md)
- [配置行项工作流](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>解决任何错误或警告

位于工作流编辑器底部的 **错误和警告** 窗格显示为工作流生成的消息。 要查找出现错误或警告的元素，请双击错误或警告消息。 必须解决所有错误和警告，然后才能激活工作流。

## <a name="save-and-activate-the-workflow"></a>保存并激活工作流

在您准备好保存和激活工作流时，请执行以下步骤。

1. 单击 **保存并关闭** 以关闭工作流编辑器并打开 **保存工作流** 页面。
2. 输入有关已对此工作流进行的更改的注释，然后单击 **确定**。
3. 如果解决了所有错误和警告，将显示 **激活工作流** 页面。 选择以下选项之一：

    - 要激活工作流的此版本，请单击 **激活新版本**。 当工作流处于活动状态下时，用户可向其提交文档进行处理。
    - 如果不希望激活该版本，请单击 **不激活新版本**。 您可以在以后激活工作流。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]