---
title: 连接试验和编辑变体
description: 本文介绍了如何将第三方服务中的试验连接到 Dynamics 365 Commerce，以及如何编辑试验的变体。
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: dcdbd61976402ddd719ece184a86692fbc7c628d
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942814"
---
# <a name="connect-an-experiment-and-edit-variations"></a>连接试验和编辑变体

本文介绍了如何在 Commerce 中连接试验和更改您的变体，以便它们与您的假设相符。 

下图显示了在 Dynamics 365 Commerce 中的电子商务网站上设置和运行试验所涉及的所有步骤。 其他步骤在单独的文章中介绍。

[![试验用户旅程 - 连接和编辑。](./media/experimentation_connect_edit.svg)](./media/experimentation_connect_edit.svg#lightbox)

在第三方服务中[设置试验](experimentation-setup.md)后，您将在 Dynamics 365 Commerce 中连接试验和编辑试验变体。

## <a name="connect-your-experiment"></a>连接试验
若要连接试验，您将启动 **连接试验** 向导。 该向导将引导您完成连接试验所需的步骤。 完成向导后，您的试验已连接，变体已创建并可以进行编辑。

若要开始在 Commerce 站点构建器中连接试验，请按照以下步骤操作。

1. 若要启动 **连接试验** 向导，请选择左侧导航窗格中的 **试验**，然后选择 **连接**。 或者，您可以通过编辑它并选择命令栏上的 **连接试验**，从页面或片段编辑器中访问该向导。

    > [!NOTE]
    > - 一个页面一次只能连接到一个试验。 若要将页面连接到其他试验，请首先删除该页面当前连接到的试验。
    > - 只有启用自定义布局的页面才能进行试验。 如果您的页面具有预设布局，请先将其转换为自定义布局。 您可以转到页面，然后在命令栏上选择 **转换为自定义布局** 来实现此目的。 有关布局的详细信息，请参阅[预设布局和自定义布局](templates-layouts-overview.md#preset-and-custom-layouts)。 

1. 如果您要从左侧导航窗格中的 **试验** 选项卡连接到试验，请从显示的列表中选择试验名称。
1. 选择您要在其上运行试验的页面或片段。
1. 在向导的最后一步中，选择 **生成变体并退出向导**。 为试验创建了变体。 

> [!NOTE]
> 如果您想要计划将试验发布到活动站点的时间，请确保在连接试验 *之前*，要与试验关联的内容在发布组中可用。 有关发布组的详细信息，请参考[使用发布组](publish-groups.md)。

## <a name="edit-your-variations"></a>编辑变体

当您退出 **Connect 试验** 向导时，会为您创建变体。 按照以下步骤编辑变体，让它们反映您需要在试验假设中验证的选择。

1. 在编辑器视图中，使用命令栏下方的变体下拉菜单，基于您的原始假设编辑每个变体。 您可能还想通过使变体之一保持不变来建立控件或基本变体。
1. 选择要在其上进行试验的模块，选择省略号 (...)，然后选择 **添加到试验**。

> [!NOTE]
> 考虑通过使变体之一保持不变来建立控件或基本变体。

## <a name="previous-step"></a>上一步
[设置试验](experimentation-setup.md) 


## <a name="next-step"></a>后续步骤
[预览和发布试验](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
