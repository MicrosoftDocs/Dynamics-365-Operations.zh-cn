---
title: 促进变体和完成试验
description: 本文介绍了如何在 Dynamics 365 Commerce 中促进成功的变体和完成试验。
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 3e9a978551622bbb14d9213f607d9dfabe42672a
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942729"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>促进变体和完成试验

本文描述了如何促进在试验中产生最佳结果的变体，以及如何完成试验。 下图显示了在 Dynamics 365 Commerce 中的电子商务网站上设置和运行试验所涉及的所有步骤。 其他步骤在单独的文章中介绍。

[![试验用户旅程 - 审查和完成。](./media/experimentation_review_complete.svg)](./media/experimentation_review_complete.svg#lightbox)

在[运行试验](experimentation-run-monitor.md)并收集了足够的数据来确定您要在活动站点上使用哪种变体后，您将促进变体并结束试验。

## <a name="promote-a-variation"></a>促进变体
使用与第三方服务中的试验相关的数据和分析来确定哪种变体产生了最佳结果。 然后您可以通过将活动站点上的当前内容替换为最佳变体，以供您的网站的所有用户使用，促进该变体。

若要促进最佳变体，请按照以下步骤操作。 

1. 在 Commerce 站点构建器中，选择左侧导航窗格中的 **试验**，然后选择试验。
1. 在命令栏上，选择 **完成试验**。
1. 在 **完成试验** 对话框中，选择 **查看试验数据**。 将打开第三方服务，您可以在其中验证指标并确定哪种变体表现最好。
1. 在 **完成试验** 对话框中，选择最佳变体，然后选择 **下一步**。
1. 打开第三方服务并停止试验。
1. 在站点构建器中，选择 **完成** 以覆盖原始活动页面并发布最佳变体，以供您的网站的所有用户使用。 

> [!NOTE]
> 如果您选择保留当前的活动页面而不发布变体，请选择 **重新发布原始页面**。

## <a name="delete-your-experiment"></a>删除试验
虽然不需要在 Commerce 中删除完成的试验，但您可以选择删除它以节省空间或清理工作区。 

若要在 Commerce 站点构建器中删除已完成的试验，请按照以下步骤操作。

1. 选择左侧导航窗格中的 **试验**，然后选择试验。 
    > [!NOTE]
    > 如果试验仍处于活动状态，请先在第三方服务中停止试验，然后再继续。
1. 在命令栏上，选择 **取消发布**，以从活动站点中删除变体内容。
1. 选择 **删除** 以删除试验。

## <a name="previous-step"></a>上一步
[运行和监控试验](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
