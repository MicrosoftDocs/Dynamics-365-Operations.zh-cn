---
title: 预览和发布试验
description: 本文介绍了如何从 Dynamics 365 Commerce 中预览和发布试验。
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 5da7a4e3c17057278d02ebd45702d1de404f0dc6
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946124"
---
# <a name="preview-and-publish-an-experiment"></a>预览和发布试验

本文介绍了如何在[连接试验和编辑变体](experimentation-connect-edit.md)之后在 Dynamics 365 Commerce 中预览和发布试验。 下图显示了在 Dynamics 365 Commerce 中的电子商务网站上设置和运行试验所涉及的所有步骤。 其他步骤在单独的文章中介绍。

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

### <a name="force-variations-for-testing"></a>强制变体进行测试

试验开始后，您可以将试验 ID 和变体 ID 追加到默认页面 URL，以强制变体进行测试或自动化。 例如，如果默认页面 URL 是 `https://fabrikam.com/modern/homepage`，您可以使用 URL（如 `https://fabrikam.com/modern/homepage?exp=18012910471|18024360464`）对变体进行强制。 您可以从上面说明的 **预览** 体验中的预览 URL 获取试验变体的试验 ID 和变体 ID。

## <a name="previous-step"></a>上一步
[连接和编辑试验](experimentation-connect-edit.md)

## <a name="next-step"></a>后续步骤
[运行和监控试验](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
