---
title: 运行和监视试验
description: 本主题介绍了如何在第三方服务中运行和监视试验。 它还介绍了如何在试验开始后更改变体。
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ee86a6761b27f3c08a65a2e250659cdcfd71db44
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2020
ms.locfileid: "4410630"
---
# <a name="run-and-monitor-an-experiment"></a>运行和监视试验

本主题介绍了如何在第三方应用中运行和监视试验，以及如何更改变体（如果需要）。 在完成本主题中的步骤之前，您首先需要在 Commerce 中[发布](experimentation-preview-publish.md)试验。 

下图显示了在 Dynamics 365 Commerce 中的电子商务网站上设置和运行试验所涉及的所有步骤。 其他步骤在单独的主题中介绍。

[![试验用户旅程 - 运行和监视](./media/experimentation_run_monitor.svg)](./media/experimentation_run_monitor.svg#lightbox)

发布变体后，完成在 Commerce 中运行试验所需的所有步骤。 下一步是确定在每个用户请求页面时向他们显示哪个变体。 第三方服务可以做出决定，但是首先您必须在服务中激活试验。 由于激活试验的步骤因服务而异，因此您需要按照服务或提供商提供的说明进行操作。 如果未激活试验，用户将仅看到页面的默认版本（不显示任何变体）。

您需要保持试验运行足够长的时间以收集数据，从而得到统计上有效的结果。 在运行试验时，使用第三方服务监视与试验相关的数据和分析。

## <a name="adjust-your-variations"></a>调整您的变体
如果出于任何原因需要修改变体，请按照以下步骤操作。

> [!IMPORTANT]
> 如果您对 Commerce 或第三方服务中的实时试验进行了更改，则结果可能会受到重大影响。 考虑继续完成试验，然后为重大更改创建新的试验。

1. 在 Commerce 站点构建器中，选择左侧导航窗格中的 **试验**，然后选择试验。 
1. 从下拉菜单中选择要更新的变体。
1. 进行任何所需的更改，然后预览和发布变体。 有关详细信息，请参阅[预览和发布试验](experimentation-preview-publish.md)。
1. 转到第三方服务以进行与试验设置相关的任何更改。
    
## <a name="previous-step"></a>上一步
[预览和发布试验](experimentation-preview-publish.md)

## <a name="next-step"></a>后续步骤
[促进变体和完成试验](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]