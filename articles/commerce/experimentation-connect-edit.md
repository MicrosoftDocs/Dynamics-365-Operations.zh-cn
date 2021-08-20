---
title: 连接试验和编辑变体
description: 本主题介绍了如何将第三方服务中的试验连接到 Dynamics 365 Commerce，以及如何编辑试验的变体。
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: d3b1a099e29073e82e2118f9e43441a9068a4d10f0ea9f79123b97d2b7d5c419
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773025"
---
# <a name="connect-an-experiment-and-edit-variations"></a>连接试验和编辑变体

本主题介绍了如何在 Commerce 中连接试验和更改您的变体，以便它们与您的假设相符。 

下图显示了在 Dynamics 365 Commerce 中的电子商务网站上设置和运行试验所涉及的所有步骤。 其他步骤在单独的主题中介绍。

[![试验用户旅程 - 连接和编辑。](./media/experimentation_connect_edit.svg)](./media/experimentation_connect_edit.svg#lightbox)

在第三方服务中[设置试验](experimentation-setup.md)后，您将在 Dynamics 365 Commerce 中连接试验和编辑试验变体。

## <a name="planning-considerations"></a>计划注意事项

在 Commerce 中连接试验之前，您需要做出一些可能影响 Commerce 管理内容的方式的决定。

### <a name="determine-the-scope-of-your-experiment"></a>确定试验范围
连接试验时，系统会提示您定义试验范围。 试验定义为 **部分** 范围或 **整个** 范围。
- 如果您要在页面的特定部分进行试验，则选择 **部分**。 如果选择此选项，必须标识试验中包括哪些模块。 对默认页面或片段中与试验无关的部分所做的更改会在变体之间自动同步。
- 如果您要在整个页面或片段上进行试验，则选择 **整个**。 将创建默认页面或片段的单独副本。 您无需选择试验中包括哪些模块，因为整个编辑界面都可以更改。 您可以根据需要添加、删除或重新排序模块。 但是，如果对与试验相关联的默认页面或片段进行了任何更改，则必须在所有变体之间手动同步这些更改。

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> 如果您将试验与使用布局的页面相关联，则只能将试验的范围设置为 **整个**。

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a>决定是否要计划发布试验的时间
如果您想要计划将试验发布到活动站点的时间，请确保在连接试验 *之前*，要与试验关联的内容在发布组中可用。 

有关发布组的详细信息，请参考[使用发布组](publish-groups.md)。


## <a name="connect-your-experiment"></a>连接试验
若要连接试验，您将启动 **连接试验** 向导。 该向导将引导您完成连接试验所需的步骤。 完成向导后，您的试验已连接，变体已创建并可以进行编辑。

若要开始在 Commerce 站点构建器中连接试验，请按照以下步骤操作。

1. 若要启动 **连接试验** 向导，请选择左侧导航窗格中的 **试验**，然后选择 **连接**。 或者，您可以通过编辑它并选择命令栏上的 **连接试验**，从页面或片段编辑器中访问该向导。

    > [!NOTE]
    > 一个页面一次只能连接到一个试验。 若要将页面连接到其他试验，请首先删除该页面当前连接到的试验。

1. 选择您要在其上运行试验的页面或片段。
1. 根据您在上述 [确定试验范围](#determine-the-scope-of-your-experiment)部分中做出的选择，将试验范围设置为 **部分** 或 **整个**。
    > [!NOTE]
    > 如果要在整个页面或片段上进行试验，则必须启用 **在页面或片段上试验** 功能标志。 有关详细信息，请参考 [Dynamics 365 Commerce 中的试验](experimentation-overview.md)主题。
    
1. 在向导的最后一步中，选择 **生成变体并退出向导**。 为试验创建了变体。 

## <a name="edit-your-variations"></a>编辑变体
退出向导时，将为您创建变体。 

接下来，您将编辑变体，以便它们反映您需要在试验假设中验证的选择。 选择与您在上述[确定试验范围](#determine-the-scope-of-your-experiment)部分中为试验选择的范围相对应的以下过程之一。

### <a name="edit-variations-for-experiments-with-partial-scope"></a>编辑具有部分范围的试验的变体
如果您在 **连接试验** 向导中将试验的范围定义为 **部分**，请执行以下步骤。

1. 在编辑器视图中，使用命令栏下方的变体下拉菜单，基于您的原始假设编辑每个变体。 您可能还想通过使变体之一保持不变来建立控件或基本变体。
1. 选择要在其上进行试验的模块，选择省略号 (...)，然后选择 **添加到试验**。

### <a name="edit-variations-for-experiments-with-entire-scope"></a>编辑具有整个范围的试验的变体
如果您在 **连接试验** 向导中将试验的范围定义为 **整个**，在编辑器视图中时，使用命令栏下方的变体下拉菜单根据您的原始假设编辑每个变体。 

> [!NOTE]
> 在任何一种情况下，您可能还想通过使变体之一保持不变来建立控件或基本变体。

## <a name="previous-step"></a>上一步
[设置试验](experimentation-setup.md) 


## <a name="next-step"></a>后续步骤
[预览和发布试验](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]