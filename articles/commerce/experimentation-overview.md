---
title: Dynamics 365 Commerce 中的试验
description: 通过试验，可以在站点构建器中创建、编辑和管理页面布局和内容处理。 为电子商务页面和页面中的实体启用了端到端试验支持。
author: sushma-rao
ms.date: 06/07/2022
ms.topic: overview
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1ef877072ba7ffe1b0326cf8d526b512b5ab30b8
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946194"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Dynamics 365 Commerce 中的试验
使用 Dynamics 365 Commerce 中的试验以验证有关您的电子商务页面有效性的假设，并以数据驱动的信心做出决策。 Commerce 支持在页面、模块和片段上进行 A/B 测试，并使您能够度量建议的更改对网站的影响。

您可以在 Commerce 站点构建器中创建、编辑和管理页面和内容处理（称为 **变体**）。 Commerce 与第三方服务集成，可用于创建试验和处理分配。 在 Commerce 中捕获的实时事件流可启用在第三方服务中定义试验结果的分析。 然后，您可以利用这些分析来帮助支持或驳倒您的假设。

## <a name="set-up-prerequisites"></a> 设置先决条件

1. **获取正确的 Commerce 版本** - 将您的模块库、在线渠道可扩展性软件开发工具包 (SDK) 和 Commerce Scale Unit 升级到 Commerce 版本 10.0.13 或更高版本。
1. **设置试验连接器** - 试验连接器允许 Commerce 与第三方服务连接，以检索试验列表并确定何时向用户展示试验。 您可以从 [AppSource](https://appsource.microsoft.com) 中购买第三方连接器。 请按照发布者提供的安装说明操作。 您也可以使用 Commerce 的示例测试连接器来测试试验工作流，而无需配置外部服务。 有关详细信息，请参阅[配置和启用连接器](e-commerce-extensibility/connectors.md)。 
1. **在 Commerce 中打开试验功能标志** - 您可以通过转到 **租户设置 \> 功能** 在租户级别上启用试验，或转到 **站点设置 \> 功能** 在站点级别启用。 打开 **试验** 标志开始创建模块变体。 禁用此标志将阻止向用户显示所有试验，并删除站点构建器中的所有编辑功能。
    
## <a name="experimentation-lifecycle"></a>试验生命周期

设置试验，创建变体和运行试验是一个迭代过程。 下图说明了 Commerce 和第三方服务中的试验生命周期。 

[ ![试验生命周期。](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

若要了解有关试验过程中每个步骤的详细信息，请参考以下文章。
- [标识假设并确定试验指标](experimentation-identify.md)
- [设计试验](experimentation-setup.md)
- [连接和编辑试验](experimentation-connect-edit.md)
- [预览并发布试验](experimentation-preview-publish.md)
- [运行和监视试验](experimentation-run-monitor.md)
- [加入变量并完成试验](experimentation-review-complete.md)

> [!NOTE]
> 若要了解试验在生命周期中的位置，请选择站点构建器的左侧导航窗格中的 **试验**。 将显示试验列表，其中包含 Commerce 和第三方服务中每个试验的状态。 有关详细信息，请参阅[查看试验的状态](experimentation-status.md)。

## <a name="next-step"></a>后续步骤
[标识假设并确定试验的成功指标](experimentation-identify.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
