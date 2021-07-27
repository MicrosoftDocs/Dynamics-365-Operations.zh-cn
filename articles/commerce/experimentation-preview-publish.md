---
title: 预览和发布试验
description: 本主题介绍了如何从 Dynamics 365 Commerce 中预览和发布试验。
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
ms.openlocfilehash: 99e873a07accd33aebfe010fbc8678cd8bc3ed9c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349296"
---
# <a name="preview-and-publish-an-experiment"></a>预览和发布试验

本主题介绍了如何在[连接试验和编辑变体](experimentation-connect-edit.md)之后在 Dynamics 365 Commerce 中预览和发布试验。 下图显示了在 Dynamics 365 Commerce 中的电子商务网站上设置和运行试验所涉及的所有步骤。 其他步骤在单独的主题中介绍。

[![试验用户旅程 - 预览和发布。](./media/experimentation_preview_publish.svg)](./media/experimentation_preview_publish.svg#lightbox)

## <a name="preview-your-experiment-variations"></a>预览试验变体
您可以预览变体并继续进行编辑，直到它们实现您的预期效果。

若要在 Commerce 站点构建器中预览试验变体，请按照以下步骤操作。

1. 从命令栏下方的变体下拉菜单中，选择要预览的内容。 
1. 在命令栏中，选择 **预览**。 显示内容发布时的预览情况。
1. 若要预览其他变体，请从变体下拉菜单中选择它，然后再次选择 **预览**。

## <a name="publish-your-experiment"></a>发布试验
如果您没有使用发布组来计划试验上线的时间，并且想立即发布，请在命令栏中选择 **发布**。 将发布属于该试验的所有变体。
    
> [!IMPORTANT]
> 如果页面上有取消发布的 URL，必须首先发布该 URL，否则它将对您的网站用户不可见。 有关详细信息，请参阅[保存、预览和发布页面](save-preview-publish-page.md)。
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a>使用发布组计划试验上线的时间
可以使用发布组计划发布在站点构建器中创建的变体。 在发布组中，您可以通过选择左侧导航窗格中的 **试验** 将页面或片段连接到试验。 您也可以通过选择 **页面** 或 **片段** 并按照[连接试验和编辑变体](experimentation-connect-edit.md)中的说明来执行此操作。 有关发布组的信息，请参阅[使用发布组](publish-groups.md)。

当使用发布组进行试验时，有一些需要注意的重要考虑事项。
- 当您将运行了试验的页面或片段添加到发布组时，该试验将从发布组的页面或片段中删除。
- 连接到活动站点中的页面的试验不适用于发布组中的页面，反之亦然。 同样，在活动站点中运行了试验的页面也不适用于发布组中的其他试验，反之亦然。
- 当您发布或计划发布组时，发布组中的所有内容都将发布，而不管是否有与发布组关联的试验。
- 由于发布组在发布到活动站点后仍会继续存在，因此发布组中的试验也将继续存在。 因此，您将无法将其他试验与同一页面或片段相关联。 为了避免此限制，请删除具有持续性试验的所有发布组。 同样，如果您要删除的试验不仅在活动站点中，也存在于发布组中，请先将其从发布组中删除。

## <a name="previous-step"></a>上一步
[连接和编辑试验](experimentation-connect-edit.md)

## <a name="next-step"></a>后续步骤
[运行和监视试验](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]