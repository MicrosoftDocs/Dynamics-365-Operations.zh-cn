---
title: 设置试验
description: 本主题介绍了如何在第三方服务中设置试验。
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
ms.openlocfilehash: 870bcb9cc63fd4dbf6d7b40d730edfad7783540d5d943896e0129d29572fa875
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769387"
---
# <a name="set-up-an-experiment"></a>设置试验

在[定义假设并确定您要使用哪些成功指标](experimentation-identify.md)后，您需要在第三方服务中设置试验。 下图显示了在 Dynamics 365 Commerce 中的电子商务网站上设置和运行试验所涉及的所有步骤。 其他步骤在单独的主题中介绍。

[![试验用户旅程 - 设置。](./media/experimentation_setup.svg)](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>在第三方服务中设置试验
到目前为止，您应该已经选择了第三方服务来运行和监视您的试验，并设置了试验连接器。 这些先决条件在 [Dynamics 365 Commerce 中的试验](experimentation-overview.md)中列出。

请按照在第三方服务中创建试验所需的步骤进行操作。 如果连接器配置正确，则您在第三方服务中设置的试验的完整列表将在大约 5 分钟内显示在 Commerce 站点构建器中。

## <a name="set-up-your-success-metrics"></a>设置您的成功指标
每个试验都需要指标来度量变体的影响和验证假设。 请按照以下步骤使用 Dynamics 365 Commerce 中的实时遥测事件来在第三方服务中启用指标计算。

若要设置成功指标，请按照以下步骤操作。

1. 在 Commerce 站点构建器中，选择左侧导航窗格中的 **页面**，然后选择要为其收集指标的页面。 
1. 转到您要跟踪的页面或模块的右侧属性窗格中的 **要跟踪的事件 ID** 部分。
1. 选择 **查看**。 显示所有事件 ID 的列表。 复制您要跟踪的事件，然后将事件密钥粘贴到第三方服务中的指定位置。 如果您需要多个事件，则一次复制一个密钥。 
    - 若要了解如何查看所有可用事件和属性，包括页面视图和收入跟踪，请参阅 [Commerce 组件的诊断和疑难解答事件](dev-itpro/retail-component-events-diagnostics-troubleshooting.md)。
1. 根据第三方服务的要求，采取任何其他步骤来跟踪指标。

## <a name="previous-step"></a>上一步
[标识假设并确定试验指标](experimentation-identify.md) 


## <a name="next-step"></a>后续步骤
[连接和编辑试验](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]